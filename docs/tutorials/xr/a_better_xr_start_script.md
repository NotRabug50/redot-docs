# A better XR start script

In `doc_setting_up_xr` we introduced a startup script that initialises
our setup which we used as our script on our main node. This script
performs the minimum steps required for any given interface.

When using OpenXR there are a number of improvements we should do here.
For this we've created a more elaborate starting script. You will find
these used in our demo projects.

Alternatively, if you are using XR Tools (see
`doc_introducing_xr_tools`) it contains a version of this script updated
with some features related to XR tools.

Below we will detail out the script used in our demos and explain the
parts that are added.

## Signals for our script

We are introducing 3 signals to our script so that our game can add
further logic:

-   `focus_lost` is emitted when the player takes off their headset or
    when the player enters the menu system of the headset.
-   `focus_gained` is emitted when the player puts their headset back on
    or exists the menu system and returns to the game.
-   `pose_recentered` is emitted when the headset requests the players
    position to be reset.

Our game should react accordingly to these signals.

.. code-tab:: gdscript GDScript

extends Node3D

signal focus\_lost signal focus\_gained signal pose\_recentered

...

csharp

using Godot;

public partial class MyNode3D : Node3D { \[Signal\] public delegate void
FocusLostEventHandler();

> \[Signal\] public delegate void FocusGainedEventHandler();
>
> \[Signal\] public delegate void PoseRecenteredEventHandler();

...

## Variables for our script

We introduce a few new variables to our script as well:

-   `maximum_refresh_rate` will control the headsets refresh rate if
    this is supported by the headset.
-   `xr_interface` holds a reference to our XR interface, this already
    existed but we now type it to get full access to our
    `XRInterface <class_xrinterface>` API.
-   `xr_is_focussed` will be set to true whenever our game has focus.

.. code-tab:: gdscript GDScript

...

@export var maximum\_refresh\_rate : int = 90

var xr\_interface : OpenXRInterface var xr\_is\_focussed = false

...

csharp

...

> \[Export\] public int MaximumRefreshRate { get; set; } = 90;
>
> private OpenXRInterface \_xrInterface;
>
> private bool \_xrIsFocused;

...

## Our updated ready function

We add a few things to the ready function.

If we're using the mobile or forward+ renderer we set the viewports
`vrs_mode` to `VRS_XR`. On platforms that support this, this will enable
foveated rendering.

If we're using the compatibility renderer, we check if the OpenXR
foveated rendering settings are configured and if not, we output a
warning. See `OpenXR Settings <doc_openxr_settings>` for further
details.

We hook up a number of signals that will be emitted by the
`XRInterface <class_xrinterface>`. We'll provide more detail about these
signals as we implement them.

We also quit our application if we couldn't successfully initialise
OpenXR. Now this can be a choice. If you are making a mixed mode game
you setup the VR mode of your game on success, and setup the non-VR mode
of your game on failure. However, when running a VR only application on
a standalone headset, it is nicer to exit on failure than to hang the
system.

.. code-tab:: gdscript GDScript

...

\# Called when the node enters the scene tree for the first time. func
\_ready(): xr\_interface = XRServer.find\_interface("OpenXR") if
xr\_interface and xr\_interface.is\_initialized(): print("OpenXR
instantiated successfully.") var vp : Viewport = get\_viewport()

> \# Enable XR on our viewport vp.use\_xr = true
>
> \# Make sure v-sync is off, v-sync is handled by OpenXR
> DisplayServer.window\_set\_vsync\_mode(DisplayServer.VSYNC\_DISABLED)
>
> \# Enable VRS if RenderingServer.get\_rendering\_device():
> vp.vrs\_mode = Viewport.VRS\_XR elif
> int(ProjectSettings.get\_setting("xr/openxr/foveation\_level")) == 0:
> push\_warning("OpenXR: Recommend setting Foveation level to High in
> Project Settings")
>
> \# Connect the OpenXR events
> xr\_interface.session\_begun.connect(\_on\_openxr\_session\_begun)
> xr\_interface.session\_visible.connect(\_on\_openxr\_visible\_state)
> xr\_interface.session\_focussed.connect(\_on\_openxr\_focused\_state)
> xr\_interface.session\_stopping.connect(\_on\_openxr\_stopping)
> xr\_interface.pose\_recentered.connect(\_on\_openxr\_pose\_recentered)
> else: \# We couldn't start OpenXR. print("OpenXR not instantiated!")
> get\_tree().quit()

...

csharp

...

> /// &lt;summary&gt; /// Called when the node enters the scene tree for
> the first time. /// &lt;/summary&gt; public override void \_Ready() {
> \_xrInterface = (OpenXRInterface)XRServer.FindInterface("OpenXR"); if
> (\_xrInterface != null && \_xrInterface.IsInitialized()) {
> GD.Print("OpenXR instantiated successfully."); var vp = GetViewport();
>
> > // Enable XR on our viewport vp.UseXR = true;
> >
> > // Make sure v-sync is off, v-sync is handled by OpenXR
> > DisplayServer.WindowSetVsyncMode(DisplayServer.VSyncMode.Disabled);
> >
> > // Enable VRS if (RenderingServer.GetRenderingDevice() != null)
> > vp.VrsMode = Viewport.VrsModeEnum.XR; else if
> > ((int)ProjectSettings.GetSetting("xr/openxr/foveation\_level") == 0)
> > GD.PushWarning("OpenXR: Recommend setting Foveation level to High in
> > Project Settings");
> >
> > // Connect the OpenXR events \_xrInterface.SessionBegun +=
> > OnOpenXRSessionBegun; \_xrInterface.SessionVisible +=
> > OnOpenXRVisibleState; \_xrInterface.SessionFocussed +=
> > OnOpenXRFocusedState; \_xrInterface.SessionStopping +=
> > OnOpenXRStopping; \_xrInterface.PoseRecentered +=
> > OnOpenXRPoseRecentered; } else { // We couldn't start OpenXR.
> > GD.Print("OpenXR not instantiated!"); GetTree().Quit(); }
>
> }

...

## On session begun

This signal is emitted by OpenXR when our session is setup. This means
the headset has run through setting everything up and is ready to begin
receiving content from us. Only at this time various information is
properly available.

The main thing we do here is to check our headsets refresh rate. We also
check the available refresh rates reported by the XR runtime to
determine if we want to set our headset to a higher refresh rate.

Finally we match our physics update rate to our headset update rate.
Godot runs at a physics update rate of 60 updates per second by default
while headsets run at a minimum of 72, and for modern headsets often up
to 144 frames per second. Not matching the physics update rate will
cause stuttering as frames are rendered without objects moving.

.. code-tab:: gdscript GDScript

...

\# Handle OpenXR session ready func \_on\_openxr\_session\_begun() -&gt;
void: \# Get the reported refresh rate var current\_refresh\_rate =
xr\_interface.get\_display\_refresh\_rate() if current\_refresh\_rate
&gt; 0: print("OpenXR: Refresh rate reported as ",
str(current\_refresh\_rate)) else: print("OpenXR: No refresh rate given
by XR runtime")

> \# See if we have a better refresh rate available var new\_rate =
> current\_refresh\_rate var available\_rates : Array =
> xr\_interface.get\_available\_display\_refresh\_rates() if
> available\_rates.size() == 0: print("OpenXR: Target does not support
> refresh rate extension") elif available\_rates.size() == 1: \# Only
> one available, so use it new\_rate = available\_rates\[0\] else: for
> rate in available\_rates: if rate &gt; new\_rate and rate &lt;=
> maximum\_refresh\_rate: new\_rate = rate
>
> \# Did we find a better rate? if current\_refresh\_rate != new\_rate:
> print("OpenXR: Setting refresh rate to ", str(new\_rate))
> xr\_interface.set\_display\_refresh\_rate(new\_rate)
> current\_refresh\_rate = new\_rate
>
> \# Now match our physics rate Engine.physics\_ticks\_per\_second =
> current\_refresh\_rate

...

csharp

...

> /// &lt;summary&gt; /// Handle OpenXR session ready ///
> &lt;/summary&gt; private void OnOpenXRSessionBegun() { // Get the
> reported refresh rate var currentRefreshRate =
> \_xrInterface.DisplayRefreshRate; GD.Print(currentRefreshRate &gt;
> 0.0F ? $"OpenXR: Refresh rate reported as {currentRefreshRate}" :
> "OpenXR: No refresh rate given by XR runtime");
>
> > // See if we have a better refresh rate available var newRate =
> > currentRefreshRate; var availableRates =
> > \_xrInterface.GetAvailableDisplayRefreshRates(); if
> > (availableRates.Count == 0) { GD.Print("OpenXR: Target does not
> > support refresh rate extension"); } else if (availableRates.Count
> > == 1) { // Only one available, so use it newRate =
> > (float)availableRates\[0\]; } else { GD.Print("OpenXR: Available
> > refresh rates: ", availableRates); foreach (float rate in
> > availableRates) if (rate &gt; newRate && rate &lt;=
> > MaximumRefreshRate) newRate = rate; }
> >
> > // Did we find a better rate? if (currentRefreshRate != newRate) {
> > GD.Print($"OpenXR: Setting refresh rate to {newRate}");
> > \_xrInterface.DisplayRefreshRate = newRate; currentRefreshRate =
> > newRate; }
> >
> > // Now match our physics rate Engine.PhysicsTicksPerSecond =
> > (int)currentRefreshRate;
>
> }

...

## On visible state

This signal is emitted by OpenXR when our game becomes visible but is
not focussed. This is a bit of a weird description in OpenXR but it
basically means that our game has just started and we're about to switch
to the focussed state next, that the user has opened a system menu or
the users has just took their headset off.

On receiving this signal we'll update our focussed state, we'll change
the process mode of our node to disabled which will pause processing on
this node and it's children, and emit our `focus_lost` signal.

If you've added this script to your root node, this means your game will
automatically pause when required. If you haven't, you can connect a
method to the signal that performs additional changes.

Note

While your game is in visible state because the user has opened a system
menu, Godot will keep rendering frames and head tracking will remain
active so your game will remain visible in the background. However
controller and hand tracking will be disabled until the user exits the
system menu.

.. code-tab:: gdscript GDScript

...

\# Handle OpenXR visible state func \_on\_openxr\_visible\_state() -&gt;
void: \# We always pass this state at startup, \# but the second time we
get this it means our player took off their headset if xr\_is\_focussed:
print("OpenXR lost focus")

> xr\_is\_focussed = false
>
> \# pause our game get\_tree().paused = true
>
> emit\_signal("focus\_lost")

...

csharp

...

> /// &lt;summary&gt; /// Handle OpenXR visible state ///
> &lt;/summary&gt; private void OnOpenXRVisibleState() { // We always
> pass this state at startup, // but the second time we get this it
> means our player took off their headset if (\_xrIsFocused) {
> GD.Print("OpenXR lost focus");
>
> > \_xrIsFocused = false;
> >
> > // Pause our game GetTree().Paused = true;
> >
> > EmitSignal(SignalName.FocusLost); }
>
> }

...

## On focussed state

This signal is emitted by OpenXR when our game gets focus. This is done
at the completion of our startup, but it can also be emitted when the
user exits a system menu, or put their headset back on.

Note also that when your game starts while the user is not wearing their
headset, the game stays in 'visible' state until the user puts their
headset on.

Warning

It is thus important to keep your game paused while in visible mode. If
you don't the game will keep on running while your user isn't
interacting with your game. Also when the game returns to focussed mode,
suddenly all controller and hand tracking is re-enabled and could have
game breaking consequences if you do not react to this accordingly. Be
sure to test this behaviour in your game!

While handling our signal we will update the focusses state, unpause our
node and emit our `focus_gained` signal.

.. code-tab:: gdscript GDScript

...

\# Handle OpenXR focused state func \_on\_openxr\_focused\_state() -&gt;
void: print("OpenXR gained focus") xr\_is\_focussed = true

> \# unpause our game get\_tree().paused = false
>
> emit\_signal("focus\_gained")

...

csharp

...

> /// &lt;summary&gt; /// Handle OpenXR focused state ///
> &lt;/summary&gt; private void OnOpenXRFocusedState() {
> GD.Print("OpenXR gained focus"); \_xrIsFocused = true;
>
> > // Un-pause our game GetTree().Paused = false;
> >
> > EmitSignal(SignalName.FocusGained);
>
> }

...

## On stopping state

This signal is emitted by OpenXR when we enter our stop state. There are
some differences between platforms when this happens. On some platforms
this is only emitted when the game is being closed. But on other
platforms this will also be emitted every time the player takes off
their headset.

For now this method is only a place holder.

.. code-tab:: gdscript GDScript

...

\# Handle OpenXR stopping state func \_on\_openxr\_stopping() -&gt;
void: \# Our session is being stopped. print("OpenXR is stopping")

...

csharp

...

> /// &lt;summary&gt; /// Handle OpenXR stopping state ///
> &lt;/summary&gt; private void OnOpenXRStopping() { // Our session is
> being stopped. GD.Print("OpenXR is stopping"); }

...

## On pose recentered

This signal is emitted by OpenXR when the user requests their view to be
recentered. Basically this communicates to your game that the user is
now facing forward and you should re-orient the player so they are
facing forward in the virtual world.

As doing so is dependent on your game, your game needs to react
accordingly.

All we do here is emit the `pose_recentered` signal. You can connect to
this signal and implement the actual recenter code. Often it is enough
to call `center_on_hmd() <class_XRServer_method_center_on_hmd>`.

.. code-tab:: gdscript GDScript

...

\# Handle OpenXR pose recentered signal func
\_on\_openxr\_pose\_recentered() -&gt; void: \# User recentered view, we
have to react to this by recentering the view. \# This is game
implementation dependent. emit\_signal("pose\_recentered")

csharp

...

> /// &lt;summary&gt; /// Handle OpenXR pose recentered signal ///
> &lt;/summary&gt; private void OnOpenXRPoseRecentered() { // User
> recentered view, we have to react to this by recentering the view. //
> This is game implementation dependent.
> EmitSignal(SignalName.PoseRecentered); }

}

And that finished our script. It was written so that it can be re-used
over multiple projects. Just add it as the script on your main node (and
extend it if needed) or add it on a child node specific for this script.
