github\_url  
hide

# Window

**Inherits:** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:** `AcceptDialog<class_AcceptDialog>`,
`Popup<class_Popup>`

Base class for all windows, dialogs, and popups.

classref-introduction-group

## Description

A node that creates a window. The window can either be a native system
window or embedded inside another **Window** (see
`Viewport.gui_embed_subwindows<class_Viewport_property_gui_embed_subwindows>`).

At runtime, **Window**s will not close automatically when requested. You
need to handle it manually using the
`close_requested<class_Window_signal_close_requested>` signal (this
applies both to pressing the close button and clicking outside of a
popup).

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Theme Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**about\_to\_popup**() `🔗<class_Window_signal_about_to_popup>`

Emitted right after `popup<class_Window_method_popup>` call, before the
**Window** appears or does anything.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**close\_requested**() `🔗<class_Window_signal_close_requested>`

Emitted when the **Window**'s close button is pressed or when
`popup_window<class_Window_property_popup_window>` is enabled and user
clicks outside the window.

This signal can be used to handle window closing, e.g. by connecting it
to `hide<class_Window_method_hide>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**dpi\_changed**() `🔗<class_Window_signal_dpi_changed>`

Emitted when the **Window**'s DPI changes as a result of OS-level
changes (e.g. moving the window from a Retina display to a lower
resolution one).

\*\*Note:\*\* Only implemented on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**files\_dropped**(files: `PackedStringArray<class_PackedStringArray>`)
`🔗<class_Window_signal_files_dropped>`

Emitted when files are dragged from the OS file manager and dropped in
the game window. The argument is a list of file paths.

Note that this method only works with native windows, i.e. the main
window and **Window**-derived nodes when
`Viewport.gui_embed_subwindows<class_Viewport_property_gui_embed_subwindows>`
is disabled in the main viewport.

Example usage:

    func _ready():
        get_viewport().files_dropped.connect(on_files_dropped)

    func on_files_dropped(files):
        print(files)

classref-item-separator

------------------------------------------------------------------------

classref-signal

**focus\_entered**() `🔗<class_Window_signal_focus_entered>`

Emitted when the **Window** gains focus.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**focus\_exited**() `🔗<class_Window_signal_focus_exited>`

Emitted when the **Window** loses its focus.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**go\_back\_requested**() `🔗<class_Window_signal_go_back_requested>`

Emitted when a go back request is sent (e.g. pressing the "Back" button
on Android), right after
`Node.NOTIFICATION_WM_GO_BACK_REQUEST<class_Node_constant_NOTIFICATION_WM_GO_BACK_REQUEST>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**mouse\_entered**() `🔗<class_Window_signal_mouse_entered>`

Emitted when the mouse cursor enters the **Window**'s visible area, that
is not occluded behind other `Control<class_Control>`s or windows,
provided its
`Viewport.gui_disable_input<class_Viewport_property_gui_disable_input>`
is `false` and regardless if it's currently focused or not.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**mouse\_exited**() `🔗<class_Window_signal_mouse_exited>`

Emitted when the mouse cursor leaves the **Window**'s visible area, that
is not occluded behind other `Control<class_Control>`s or windows,
provided its
`Viewport.gui_disable_input<class_Viewport_property_gui_disable_input>`
is `false` and regardless if it's currently focused or not.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**theme\_changed**() `🔗<class_Window_signal_theme_changed>`

Emitted when the
`NOTIFICATION_THEME_CHANGED<class_Window_constant_NOTIFICATION_THEME_CHANGED>`
notification is sent.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**titlebar\_changed**() `🔗<class_Window_signal_titlebar_changed>`

Emitted when window title bar decorations are changed, e.g. macOS window
enter/exit full screen mode, or extend-to-title flag is changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**visibility\_changed**() `🔗<class_Window_signal_visibility_changed>`

Emitted when **Window** is made visible or disappears.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**window\_input**(event: `InputEvent<class_InputEvent>`)
`🔗<class_Window_signal_window_input>`

Emitted when the **Window** is currently focused and receives any input,
passing the received event as an argument. The event's position, if
present, is in the embedder's coordinate system.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Mode**: `🔗<enum_Window_Mode>`

classref-enumeration-constant

`Mode<enum_Window_Mode>` **MODE\_WINDOWED** = `0`

Windowed mode, i.e. **Window** doesn't occupy the whole screen (unless
set to the size of the screen).

classref-enumeration-constant

`Mode<enum_Window_Mode>` **MODE\_MINIMIZED** = `1`

Minimized window mode, i.e. **Window** is not visible and available on
window manager's window list. Normally happens when the minimize button
is pressed.

classref-enumeration-constant

`Mode<enum_Window_Mode>` **MODE\_MAXIMIZED** = `2`

Maximized window mode, i.e. **Window** will occupy whole screen area
except task bar and still display its borders. Normally happens when the
maximize button is pressed.

classref-enumeration-constant

`Mode<enum_Window_Mode>` **MODE\_FULLSCREEN** = `3`

Full screen mode with full multi-window support.

Full screen window covers the entire display area of a screen and has no
decorations. The display's video mode is not changed.

\*\*On Windows:\*\* Multi-window full-screen mode has a 1px border of
the
`ProjectSettings.rendering/environment/defaults/default_clear_color<class_ProjectSettings_property_rendering/environment/defaults/default_clear_color>`
color.

\*\*On macOS:\*\* A new desktop is used to display the running project.

\*\*Note:\*\* Regardless of the platform, enabling full screen will
change the window size to match the monitor's size. Therefore, make sure
your project supports
`multiple resolutions <../tutorials/rendering/multiple_resolutions>`
when enabling full screen mode.

classref-enumeration-constant

`Mode<enum_Window_Mode>` **MODE\_EXCLUSIVE\_FULLSCREEN** = `4`

A single window full screen mode. This mode has less overhead, but only
one window can be open on a given screen at a time (opening a child
window or application switching will trigger a full screen transition).

Full screen window covers the entire display area of a screen and has no
border or decorations. The display's video mode is not changed.

\*\*On Windows:\*\* Depending on video driver, full screen transition
might cause screens to go black for a moment.

\*\*On macOS:\*\* A new desktop is used to display the running project.
Exclusive full screen mode prevents Dock and Menu from showing up when
the mouse pointer is hovering the edge of the screen.

\*\*On Linux (X11):\*\* Exclusive full screen mode bypasses compositor.

\*\*Note:\*\* Regardless of the platform, enabling full screen will
change the window size to match the monitor's size. Therefore, make sure
your project supports
`multiple resolutions <../tutorials/rendering/multiple_resolutions>`
when enabling full screen mode.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Flags**: `🔗<enum_Window_Flags>`

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_RESIZE\_DISABLED** = `0`

The window can't be resized by dragging its resize grip. It's still
possible to resize the window using `size<class_Window_property_size>`.
This flag is ignored for full screen windows. Set with
`unresizable<class_Window_property_unresizable>`.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_BORDERLESS** = `1`

The window do not have native title bar and other decorations. This flag
is ignored for full-screen windows. Set with
`borderless<class_Window_property_borderless>`.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_ALWAYS\_ON\_TOP** = `2`

The window is floating on top of all other windows. This flag is ignored
for full-screen windows. Set with
`always_on_top<class_Window_property_always_on_top>`.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_TRANSPARENT** = `3`

The window background can be transparent. Set with
`transparent<class_Window_property_transparent>`.

\*\*Note:\*\* This flag has no effect if either
`ProjectSettings.display/window/per_pixel_transparency/allowed<class_ProjectSettings_property_display/window/per_pixel_transparency/allowed>`,
or the window's
`Viewport.transparent_bg<class_Viewport_property_transparent_bg>` is set
to `false`.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_NO\_FOCUS** = `4`

The window can't be focused. No-focus window will ignore all input,
except mouse clicks. Set with
`unfocusable<class_Window_property_unfocusable>`.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_POPUP** = `5`

Window is part of menu or `OptionButton<class_OptionButton>` dropdown.
This flag can't be changed when the window is visible. An active popup
window will exclusively receive all input, without stealing focus from
its parent. Popup windows are automatically closed when uses click
outside it, or when an application is switched. Popup window must have
transient parent set (see `transient<class_Window_property_transient>`).

\*\*Note:\*\* This flag has no effect in embedded windows (unless said
window is a `Popup<class_Popup>`).

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_EXTEND\_TO\_TITLE** = `6`

Window content is expanded to the full size of the window. Unlike
borderless window, the frame is left intact and can be used to resize
the window, title bar is transparent, but have minimize/maximize/close
buttons. Set with
`extend_to_title<class_Window_property_extend_to_title>`.

\*\*Note:\*\* This flag is implemented only on macOS.

\*\*Note:\*\* This flag has no effect in embedded windows.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_MOUSE\_PASSTHROUGH** = `7`

All mouse events are passed to the underlying window of the same
application.

\*\*Note:\*\* This flag has no effect in embedded windows.

classref-enumeration-constant

`Flags<enum_Window_Flags>` **FLAG\_MAX** = `8`

Max value of the `Flags<enum_Window_Flags>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ContentScaleMode**: `🔗<enum_Window_ContentScaleMode>`

classref-enumeration-constant

`ContentScaleMode<enum_Window_ContentScaleMode>`
**CONTENT\_SCALE\_MODE\_DISABLED** = `0`

The content will not be scaled to match the **Window**'s size.

classref-enumeration-constant

`ContentScaleMode<enum_Window_ContentScaleMode>`
**CONTENT\_SCALE\_MODE\_CANVAS\_ITEMS** = `1`

The content will be rendered at the target size. This is more
performance-expensive than
`CONTENT_SCALE_MODE_VIEWPORT<class_Window_constant_CONTENT_SCALE_MODE_VIEWPORT>`,
but provides better results.

classref-enumeration-constant

`ContentScaleMode<enum_Window_ContentScaleMode>`
**CONTENT\_SCALE\_MODE\_VIEWPORT** = `2`

The content will be rendered at the base size and then scaled to the
target size. More performant than
`CONTENT_SCALE_MODE_CANVAS_ITEMS<class_Window_constant_CONTENT_SCALE_MODE_CANVAS_ITEMS>`,
but results in pixelated image.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ContentScaleAspect**: `🔗<enum_Window_ContentScaleAspect>`

classref-enumeration-constant

`ContentScaleAspect<enum_Window_ContentScaleAspect>`
**CONTENT\_SCALE\_ASPECT\_IGNORE** = `0`

The aspect will be ignored. Scaling will simply stretch the content to
fit the target size.

classref-enumeration-constant

`ContentScaleAspect<enum_Window_ContentScaleAspect>`
**CONTENT\_SCALE\_ASPECT\_KEEP** = `1`

The content's aspect will be preserved. If the target size has different
aspect from the base one, the image will be centered and black bars will
appear on left and right sides.

classref-enumeration-constant

`ContentScaleAspect<enum_Window_ContentScaleAspect>`
**CONTENT\_SCALE\_ASPECT\_KEEP\_WIDTH** = `2`

The content can be expanded vertically. Scaling horizontally will result
in keeping the width ratio and then black bars on left and right sides.

classref-enumeration-constant

`ContentScaleAspect<enum_Window_ContentScaleAspect>`
**CONTENT\_SCALE\_ASPECT\_KEEP\_HEIGHT** = `3`

The content can be expanded horizontally. Scaling vertically will result
in keeping the height ratio and then black bars on top and bottom sides.

classref-enumeration-constant

`ContentScaleAspect<enum_Window_ContentScaleAspect>`
**CONTENT\_SCALE\_ASPECT\_EXPAND** = `4`

The content's aspect will be preserved. If the target size has different
aspect from the base one, the content will stay in the top-left corner
and add an extra visible area in the stretched space.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ContentScaleStretch**: `🔗<enum_Window_ContentScaleStretch>`

classref-enumeration-constant

`ContentScaleStretch<enum_Window_ContentScaleStretch>`
**CONTENT\_SCALE\_STRETCH\_FRACTIONAL** = `0`

The content will be stretched according to a fractional factor. This
fills all the space available in the window, but allows "pixel wobble"
to occur due to uneven pixel scaling.

classref-enumeration-constant

`ContentScaleStretch<enum_Window_ContentScaleStretch>`
**CONTENT\_SCALE\_STRETCH\_INTEGER** = `1`

The content will be stretched only according to an integer factor,
preserving sharp pixels. This may leave a black background visible on
the window's edges depending on the window size.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LayoutDirection**: `🔗<enum_Window_LayoutDirection>`

classref-enumeration-constant

`LayoutDirection<enum_Window_LayoutDirection>`
**LAYOUT\_DIRECTION\_INHERITED** = `0`

Automatic layout direction, determined from the parent window layout
direction.

classref-enumeration-constant

`LayoutDirection<enum_Window_LayoutDirection>`
**LAYOUT\_DIRECTION\_LOCALE** = `1`

Automatic layout direction, determined from the current locale.

classref-enumeration-constant

`LayoutDirection<enum_Window_LayoutDirection>`
**LAYOUT\_DIRECTION\_LTR** = `2`

Left-to-right layout direction.

classref-enumeration-constant

`LayoutDirection<enum_Window_LayoutDirection>`
**LAYOUT\_DIRECTION\_RTL** = `3`

Right-to-left layout direction.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **WindowInitialPosition**: `🔗<enum_Window_WindowInitialPosition>`

classref-enumeration-constant

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**WINDOW\_INITIAL\_POSITION\_ABSOLUTE** = `0`

Initial window position is determined by
`position<class_Window_property_position>`.

classref-enumeration-constant

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**WINDOW\_INITIAL\_POSITION\_CENTER\_PRIMARY\_SCREEN** = `1`

Initial window position is the center of the primary screen.

classref-enumeration-constant

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**WINDOW\_INITIAL\_POSITION\_CENTER\_MAIN\_WINDOW\_SCREEN** = `2`

Initial window position is the center of the main window screen.

classref-enumeration-constant

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**WINDOW\_INITIAL\_POSITION\_CENTER\_OTHER\_SCREEN** = `3`

Initial window position is the center of
`current_screen<class_Window_property_current_screen>` screen.

classref-enumeration-constant

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**WINDOW\_INITIAL\_POSITION\_CENTER\_SCREEN\_WITH\_MOUSE\_FOCUS** = `4`

Initial window position is the center of the screen containing the mouse
pointer.

classref-enumeration-constant

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**WINDOW\_INITIAL\_POSITION\_CENTER\_SCREEN\_WITH\_KEYBOARD\_FOCUS** =
`5`

Initial window position is the center of the screen containing the
window with the keyboard focus.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_VISIBILITY\_CHANGED** = `30`
`🔗<class_Window_constant_NOTIFICATION_VISIBILITY_CHANGED>`

Emitted when **Window**'s visibility changes, right before
`visibility_changed<class_Window_signal_visibility_changed>`.

classref-constant

**NOTIFICATION\_THEME\_CHANGED** = `32`
`🔗<class_Window_constant_NOTIFICATION_THEME_CHANGED>`

Sent when the node needs to refresh its theme items. This happens in one
of the following cases:

-   The `theme<class_Window_property_theme>` property is changed on this
    node or any of its ancestors.
-   The
    `theme_type_variation<class_Window_property_theme_type_variation>`
    property is changed on this node.
-   The node enters the scene tree.

\*\*Note:\*\* As an optimization, this notification won't be sent from
changes that occur while this node is outside of the scene tree.
Instead, all of the theme item updates can be applied at once when the
node enters the scene tree.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **always\_on\_top** = `false`
`🔗<class_Window_property_always_on_top>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the window will be on top of all other windows. Does not work
if `transient<class_Window_property_transient>` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **auto\_translate** = `true`
`🔗<class_Window_property_auto_translate>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_translate**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_auto\_translating**()

**Deprecated:** Use
`Node.auto_translate_mode<class_Node_property_auto_translate_mode>`
instead.

Toggles if any text should automatically change to its translated
version depending on the current locale.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **borderless** = `false`
`🔗<class_Window_property_borderless>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the window will have no borders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ContentScaleAspect<enum_Window_ContentScaleAspect>`
**content\_scale\_aspect** = `0`
`🔗<class_Window_property_content_scale_aspect>`

classref-property-setget

-   `void (No return value.)` **set\_content\_scale\_aspect**(value:
    `ContentScaleAspect<enum_Window_ContentScaleAspect>`)
-   `ContentScaleAspect<enum_Window_ContentScaleAspect>`
    **get\_content\_scale\_aspect**()

Specifies how the content's aspect behaves when the **Window** is
resized. The base aspect is determined by
`content_scale_size<class_Window_property_content_scale_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **content\_scale\_factor** = `1.0`
`🔗<class_Window_property_content_scale_factor>`

classref-property-setget

-   `void (No return value.)` **set\_content\_scale\_factor**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_content\_scale\_factor**()

Specifies the base scale of **Window**'s content when its
`size<class_Window_property_size>` is equal to
`content_scale_size<class_Window_property_content_scale_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ContentScaleMode<enum_Window_ContentScaleMode>`
**content\_scale\_mode** = `0`
`🔗<class_Window_property_content_scale_mode>`

classref-property-setget

-   `void (No return value.)` **set\_content\_scale\_mode**(value:
    `ContentScaleMode<enum_Window_ContentScaleMode>`)
-   `ContentScaleMode<enum_Window_ContentScaleMode>`
    **get\_content\_scale\_mode**()

Specifies how the content is scaled when the **Window** is resized.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **content\_scale\_size** = `Vector2i(0, 0)`
`🔗<class_Window_property_content_scale_size>`

classref-property-setget

-   `void (No return value.)` **set\_content\_scale\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_content\_scale\_size**()

Base size of the content (i.e. nodes that are drawn inside the window).
If non-zero, **Window**'s content will be scaled when the window is
resized to a different size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ContentScaleStretch<enum_Window_ContentScaleStretch>`
**content\_scale\_stretch** = `0`
`🔗<class_Window_property_content_scale_stretch>`

classref-property-setget

-   `void (No return value.)` **set\_content\_scale\_stretch**(value:
    `ContentScaleStretch<enum_Window_ContentScaleStretch>`)
-   `ContentScaleStretch<enum_Window_ContentScaleStretch>`
    **get\_content\_scale\_stretch**()

The policy to use to determine the final scale factor for 2D elements.
This affects how
`content_scale_factor<class_Window_property_content_scale_factor>` is
applied, in addition to the automatic scale factor determined by
`content_scale_size<class_Window_property_content_scale_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **current\_screen**
`🔗<class_Window_property_current_screen>`

classref-property-setget

-   `void (No return value.)` **set\_current\_screen**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_current\_screen**()

The screen the window is currently on.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **exclusive** = `false`
`🔗<class_Window_property_exclusive>`

classref-property-setget

-   `void (No return value.)` **set\_exclusive**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_exclusive**()

If `true`, the **Window** will be in exclusive mode. Exclusive windows
are always on top of their parent and will block all input going to the
parent **Window**.

Needs `transient<class_Window_property_transient>` enabled to work.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **extend\_to\_title** = `false`
`🔗<class_Window_property_extend_to_title>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the **Window** contents is expanded to the full size of the
window, window title bar is transparent.

\*\*Note:\*\* This property is implemented only on macOS.

\*\*Note:\*\* This property only works with native windows.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **force\_native** = `false`
`🔗<class_Window_property_force_native>`

classref-property-setget

-   `void (No return value.)` **set\_force\_native**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_force\_native**()

If `true`, native window will be used regardless of parent viewport and
project settings.

classref-item-separator

------------------------------------------------------------------------

classref-property

`WindowInitialPosition<enum_Window_WindowInitialPosition>`
**initial\_position** = `0` `🔗<class_Window_property_initial_position>`

classref-property-setget

-   `void (No return value.)` **set\_initial\_position**(value:
    `WindowInitialPosition<enum_Window_WindowInitialPosition>`)
-   `WindowInitialPosition<enum_Window_WindowInitialPosition>`
    **get\_initial\_position**()

Specifies the initial type of position for the **Window**. See
`WindowInitialPosition<enum_Window_WindowInitialPosition>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **keep\_title\_visible** = `false`
`🔗<class_Window_property_keep_title_visible>`

classref-property-setget

-   `void (No return value.)` **set\_keep\_title\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_keep\_title\_visible**()

If `true`, the **Window** width is expanded to keep the title bar text
fully visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **max\_size** = `Vector2i(0, 0)`
`🔗<class_Window_property_max_size>`

classref-property-setget

-   `void (No return value.)` **set\_max\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_max\_size**()

If non-zero, the **Window** can't be resized to be bigger than this
size.

\*\*Note:\*\* This property will be ignored if the value is lower than
`min_size<class_Window_property_min_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **min\_size** = `Vector2i(0, 0)`
`🔗<class_Window_property_min_size>`

classref-property-setget

-   `void (No return value.)` **set\_min\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_min\_size**()

If non-zero, the **Window** can't be resized to be smaller than this
size.

\*\*Note:\*\* This property will be ignored in favor of
`get_contents_minimum_size<class_Window_method_get_contents_minimum_size>`
if `wrap_controls<class_Window_property_wrap_controls>` is enabled and
if its size is bigger.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mode<enum_Window_Mode>` **mode** = `0` `🔗<class_Window_property_mode>`

classref-property-setget

-   `void (No return value.)` **set\_mode**(value:
    `Mode<enum_Window_Mode>`)
-   `Mode<enum_Window_Mode>` **get\_mode**()

Set's the window's current mode.

\*\*Note:\*\* Fullscreen mode is not exclusive full screen on Windows
and Linux.

\*\*Note:\*\* This method only works with native windows, i.e. the main
window and **Window**-derived nodes when
`Viewport.gui_embed_subwindows<class_Viewport_property_gui_embed_subwindows>`
is disabled in the main viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **mouse\_passthrough** = `false`
`🔗<class_Window_property_mouse_passthrough>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, all mouse events will be passed to the underlying window of
the same application. See also
`mouse_passthrough_polygon<class_Window_property_mouse_passthrough_polygon>`.

\*\*Note:\*\* This property is implemented on Linux (X11), macOS and
Windows.

\*\*Note:\*\* This property only works with native windows.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>`
**mouse\_passthrough\_polygon** = `PackedVector2Array()`
`🔗<class_Window_property_mouse_passthrough_polygon>`

classref-property-setget

-   `void (No return value.)`
    **set\_mouse\_passthrough\_polygon**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>`
    **get\_mouse\_passthrough\_polygon**()

Sets a polygonal region of the window which accepts mouse events. Mouse
events outside the region will be passed through.

Passing an empty array will disable passthrough support (all mouse
events will be intercepted by the window, which is the default
behavior).

gdscript

\# Set region, using Path2D node. $Window.mouse\_passthrough\_polygon =
$Path2D.curve.get\_baked\_points()

\# Set region, using Polygon2D node. $Window.mouse\_passthrough\_polygon
= $Polygon2D.polygon

\# Reset region to default. $Window.mouse\_passthrough\_polygon = \[\]

csharp

// Set region, using Path2D node.
GetNode&lt;Window&gt;("Window").MousePassthrough =
GetNode&lt;Path2D&gt;("Path2D").Curve.GetBakedPoints();

// Set region, using Polygon2D node.
GetNode&lt;Window&gt;("Window").MousePassthrough =
GetNode&lt;Polygon2D&gt;("Polygon2D").Polygon;

// Reset region to default.
GetNode&lt;Window&gt;("Window").MousePassthrough = new Vector2\[\] {};

\*\*Note:\*\* This property is ignored if
`mouse_passthrough<class_Window_property_mouse_passthrough>` is set to
`true`.

\*\*Note:\*\* On Windows, the portion of a window that lies outside the
region is not drawn, while on Linux (X11) and macOS it is.

\*\*Note:\*\* This property is implemented on Linux (X11), macOS and
Windows.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **popup\_window** = `false`
`🔗<class_Window_property_popup_window>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the **Window** will be considered a popup. Popups are
sub-windows that don't show as separate windows in system's window
manager's window list and will send close request when anything is
clicked outside of them (unless
`exclusive<class_Window_property_exclusive>` is enabled).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **position** = `Vector2i(0, 0)`
`🔗<class_Window_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_position**()

The window's position in pixels.

If
`ProjectSettings.display/window/subwindows/embed_subwindows<class_ProjectSettings_property_display/window/subwindows/embed_subwindows>`
is `false`, the position is in absolute screen coordinates. This
typically applies to editor plugins. If the setting is `true`, the
window's position is in the coordinates of its parent
`Viewport<class_Viewport>`.

\*\*Note:\*\* This property only works if
`initial_position<class_Window_property_initial_position>` is set to
`WINDOW_INITIAL_POSITION_ABSOLUTE<class_Window_constant_WINDOW_INITIAL_POSITION_ABSOLUTE>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **size** = `Vector2i(100, 100)`
`🔗<class_Window_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_size**()

The window's size in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Theme<class_Theme>` **theme** `🔗<class_Window_property_theme>`

classref-property-setget

-   `void (No return value.)` **set\_theme**(value:
    `Theme<class_Theme>`)
-   `Theme<class_Theme>` **get\_theme**()

The `Theme<class_Theme>` resource this node and all its
`Control<class_Control>` and **Window** children use. If a child node
has its own `Theme<class_Theme>` resource set, theme items are merged
with child's definitions having higher priority.

\*\*Note:\*\* **Window** styles will have no effect unless the window is
embedded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **theme\_type\_variation** = `&""`
`🔗<class_Window_property_theme_type_variation>`

classref-property-setget

-   `void (No return value.)` **set\_theme\_type\_variation**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_theme\_type\_variation**()

The name of a theme type variation used by this **Window** to look up
its own theme items. See
`Control.theme_type_variation<class_Control_property_theme_type_variation>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **title** = `""`
`🔗<class_Window_property_title>`

classref-property-setget

-   `void (No return value.)` **set\_title**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_title**()

The window's title. If the **Window** is native, title styles set in
`Theme<class_Theme>` will have no effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **transient** = `false`
`🔗<class_Window_property_transient>`

classref-property-setget

-   `void (No return value.)` **set\_transient**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_transient**()

If `true`, the **Window** is transient, i.e. it's considered a child of
another **Window**. The transient window will be destroyed with its
transient parent and will return focus to their parent when closed. The
transient window is displayed on top of a non-exclusive full-screen
parent window. Transient windows can't enter full-screen mode.

Note that behavior might be different depending on the platform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **transient\_to\_focused** = `false`
`🔗<class_Window_property_transient_to_focused>`

classref-property-setget

-   `void (No return value.)` **set\_transient\_to\_focused**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_transient\_to\_focused**()

If `true`, and the **Window** is
`transient<class_Window_property_transient>`, this window will (at the
time of becoming visible) become transient to the currently focused
window instead of the immediate parent window in the hierarchy. Note
that the transient parent is assigned at the time this window becomes
visible, so changing it afterwards has no effect until re-shown.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **transparent** = `false`
`🔗<class_Window_property_transparent>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the **Window**'s background can be transparent. This is best
used with embedded windows.

\*\*Note:\*\* Transparency support is implemented on Linux, macOS and
Windows, but availability might vary depending on GPU driver, display
manager, and compositor capabilities.

\*\*Note:\*\* This property has no effect if
`ProjectSettings.display/window/per_pixel_transparency/allowed<class_ProjectSettings_property_display/window/per_pixel_transparency/allowed>`
is set to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **unfocusable** = `false`
`🔗<class_Window_property_unfocusable>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the **Window** can't be focused nor interacted with. It can
still be visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **unresizable** = `false`
`🔗<class_Window_property_unresizable>`

classref-property-setget

-   `void (No return value.)` **set\_flag**(flag:
    `Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the window can't be resized. Minimize and maximize buttons
are disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **visible** = `true`
`🔗<class_Window_property_visible>`

classref-property-setget

-   `void (No return value.)` **set\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visible**()

If `true`, the window is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **wrap\_controls** = `false`
`🔗<class_Window_property_wrap_controls>`

classref-property-setget

-   `void (No return value.)` **set\_wrap\_controls**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_wrapping\_controls**()

If `true`, the window's size will automatically update when a child node
is added or removed, ignoring `min_size<class_Window_property_min_size>`
if the new size is bigger.

If `false`, you need to call
`child_controls_changed<class_Window_method_child_controls_changed>`
manually.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Vector2<class_Vector2>` **\_get\_contents\_minimum\_size**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_private_method__get_contents_minimum_size>`

Virtual method to be implemented by the user. Overrides the value
returned by
`get_contents_minimum_size<class_Window_method_get_contents_minimum_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_color\_override**(name:
`StringName<class_StringName>`, color: `Color<class_Color>`)
`🔗<class_Window_method_add_theme_color_override>`

Creates a local override for a theme `Color<class_Color>` with the
specified `name`. Local overrides always take precedence when fetching
theme items for the control. An override can be removed with
`remove_theme_color_override<class_Window_method_remove_theme_color_override>`.

See also `get_theme_color<class_Window_method_get_theme_color>` and
`Control.add_theme_color_override<class_Control_method_add_theme_color_override>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_constant\_override**(name:
`StringName<class_StringName>`, constant: `int<class_int>`)
`🔗<class_Window_method_add_theme_constant_override>`

Creates a local override for a theme constant with the specified `name`.
Local overrides always take precedence when fetching theme items for the
control. An override can be removed with
`remove_theme_constant_override<class_Window_method_remove_theme_constant_override>`.

See also `get_theme_constant<class_Window_method_get_theme_constant>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_font\_override**(name:
`StringName<class_StringName>`, font: `Font<class_Font>`)
`🔗<class_Window_method_add_theme_font_override>`

Creates a local override for a theme `Font<class_Font>` with the
specified `name`. Local overrides always take precedence when fetching
theme items for the control. An override can be removed with
`remove_theme_font_override<class_Window_method_remove_theme_font_override>`.

See also `get_theme_font<class_Window_method_get_theme_font>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_font\_size\_override**(name:
`StringName<class_StringName>`, font\_size: `int<class_int>`)
`🔗<class_Window_method_add_theme_font_size_override>`

Creates a local override for a theme font size with the specified
`name`. Local overrides always take precedence when fetching theme items
for the control. An override can be removed with
`remove_theme_font_size_override<class_Window_method_remove_theme_font_size_override>`.

See also `get_theme_font_size<class_Window_method_get_theme_font_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_icon\_override**(name:
`StringName<class_StringName>`, texture: `Texture2D<class_Texture2D>`)
`🔗<class_Window_method_add_theme_icon_override>`

Creates a local override for a theme icon with the specified `name`.
Local overrides always take precedence when fetching theme items for the
control. An override can be removed with
`remove_theme_icon_override<class_Window_method_remove_theme_icon_override>`.

See also `get_theme_icon<class_Window_method_get_theme_icon>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_stylebox\_override**(name:
`StringName<class_StringName>`, stylebox: `StyleBox<class_StyleBox>`)
`🔗<class_Window_method_add_theme_stylebox_override>`

Creates a local override for a theme `StyleBox<class_StyleBox>` with the
specified `name`. Local overrides always take precedence when fetching
theme items for the control. An override can be removed with
`remove_theme_stylebox_override<class_Window_method_remove_theme_stylebox_override>`.

See also `get_theme_stylebox<class_Window_method_get_theme_stylebox>`
and
`Control.add_theme_stylebox_override<class_Control_method_add_theme_stylebox_override>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **begin\_bulk\_theme\_override**()
`🔗<class_Window_method_begin_bulk_theme_override>`

Prevents `*_theme_*_override` methods from emitting
`NOTIFICATION_THEME_CHANGED<class_Window_constant_NOTIFICATION_THEME_CHANGED>`
until
`end_bulk_theme_override<class_Window_method_end_bulk_theme_override>`
is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **can\_draw**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_can_draw>`

Returns whether the window is being drawn to the screen.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **child\_controls\_changed**()
`🔗<class_Window_method_child_controls_changed>`

Requests an update of the **Window** size to fit underlying
`Control<class_Control>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **end\_bulk\_theme\_override**()
`🔗<class_Window_method_end_bulk_theme_override>`

Ends a bulk theme override update. See
`begin_bulk_theme_override<class_Window_method_begin_bulk_theme_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_contents\_minimum\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_contents_minimum_size>`

Returns the combined minimum size from the child
`Control<class_Control>` nodes of the window. Use
`child_controls_changed<class_Window_method_child_controls_changed>` to
update it when child nodes have changed.

The value returned by this method can be overridden with
`_get_contents_minimum_size<class_Window_private_method__get_contents_minimum_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_flag**(flag: `Flags<enum_Window_Flags>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_flag>`

Returns `true` if the `flag` is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`LayoutDirection<enum_Window_LayoutDirection>`
**get\_layout\_direction**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_layout_direction>`

Returns layout direction and text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_position\_with\_decorations**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_position_with_decorations>`

Returns the window's position including its border.

\*\*Note:\*\* If `visible<class_Window_property_visible>` is `false`,
this method returns the same value as
`position<class_Window_property_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_size\_with\_decorations**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_size_with_decorations>`

Returns the window's size including its border.

\*\*Note:\*\* If `visible<class_Window_property_visible>` is `false`,
this method returns the same value as
`size<class_Window_property_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_theme\_color**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_color>`

Returns a `Color<class_Color>` from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
color item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_theme\_constant**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_constant>`

Returns a constant from the first matching `Theme<class_Theme>` in the
tree if that `Theme<class_Theme>` has a constant item with the specified
`name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_theme\_default\_base\_scale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_default_base_scale>`

Returns the default base scale value from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
valid
`Theme.default_base_scale<class_Theme_property_default_base_scale>`
value.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Font<class_Font>` **get\_theme\_default\_font**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_default_font>`

Returns the default font from the first matching `Theme<class_Theme>` in
the tree if that `Theme<class_Theme>` has a valid
`Theme.default_font<class_Theme_property_default_font>` value.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_theme\_default\_font\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_default_font_size>`

Returns the default font size value from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
valid `Theme.default_font_size<class_Theme_property_default_font_size>`
value.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Font<class_Font>` **get\_theme\_font**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_font>`

Returns a `Font<class_Font>` from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a font
item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_theme\_font\_size**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_font_size>`

Returns a font size from the first matching `Theme<class_Theme>` in the
tree if that `Theme<class_Theme>` has a font size item with the
specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_theme\_icon**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_icon>`

Returns an icon from the first matching `Theme<class_Theme>` in the tree
if that `Theme<class_Theme>` has an icon item with the specified `name`
and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StyleBox<class_StyleBox>` **get\_theme\_stylebox**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_theme_stylebox>`

Returns a `StyleBox<class_StyleBox>` from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
stylebox item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_window\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_get_window_id>`

Returns the ID of the window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **grab\_focus**()
`🔗<class_Window_method_grab_focus>`

Causes the window to grab focus, allowing it to receive user input.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_focus**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_focus>`

Returns `true` if the window is focused.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_color**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_color>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a color item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_color\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_color_override>`

Returns `true` if there is a local override for a theme
`Color<class_Color>` with the specified `name` in this
`Control<class_Control>` node.

See
`add_theme_color_override<class_Window_method_add_theme_color_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_constant**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_constant>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a constant item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_constant\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_constant_override>`

Returns `true` if there is a local override for a theme constant with
the specified `name` in this `Control<class_Control>` node.

See
`add_theme_constant_override<class_Window_method_add_theme_constant_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_font>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a font item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_font_override>`

Returns `true` if there is a local override for a theme
`Font<class_Font>` with the specified `name` in this
`Control<class_Control>` node.

See
`add_theme_font_override<class_Window_method_add_theme_font_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font\_size**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_font_size>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a font size item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font\_size\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_font_size_override>`

Returns `true` if there is a local override for a theme font size with
the specified `name` in this `Control<class_Control>` node.

See
`add_theme_font_size_override<class_Window_method_add_theme_font_size_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_icon**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_icon>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has an icon item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_icon\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_icon_override>`

Returns `true` if there is a local override for a theme icon with the
specified `name` in this `Control<class_Control>` node.

See
`add_theme_icon_override<class_Window_method_add_theme_icon_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_stylebox**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_stylebox>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a stylebox item with the specified `name` and `theme_type`.

See `Control.get_theme_color<class_Control_method_get_theme_color>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_stylebox\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_has_theme_stylebox_override>`

Returns `true` if there is a local override for a theme
`StyleBox<class_StyleBox>` with the specified `name` in this
`Control<class_Control>` node.

See
`add_theme_stylebox_override<class_Window_method_add_theme_stylebox_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hide**() `🔗<class_Window_method_hide>`

Hides the window. This is not the same as minimized state. Hidden window
can't be interacted with and needs to be made visible with
`show<class_Window_method_show>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_embedded**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_is_embedded>`

Returns `true` if the window is currently embedded in another window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_layout\_rtl**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_is_layout_rtl>`

Returns `true` if layout is right-to-left.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_maximize\_allowed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_is_maximize_allowed>`

Returns `true` if the window can be maximized (the maximize button is
enabled).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_using\_font\_oversampling**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Window_method_is_using_font_oversampling>`

Returns `true` if font oversampling is enabled. See
`set_use_font_oversampling<class_Window_method_set_use_font_oversampling>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_to\_center**()
`🔗<class_Window_method_move_to_center>`

Centers a native window on the current screen and an embedded window on
its embedder `Viewport<class_Viewport>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_to\_foreground**()
`🔗<class_Window_method_move_to_foreground>`

**Deprecated:** Use `grab_focus<class_Window_method_grab_focus>`
instead.

Causes the window to grab focus, allowing it to receive user input.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup**(rect: `Rect2i<class_Rect2i>` =
Rect2i(0, 0, 0, 0)) `🔗<class_Window_method_popup>`

Shows the **Window** and makes it transient (see
`transient<class_Window_property_transient>`). If `rect` is provided, it
will be set as the **Window**'s size. Fails if called on the main
window.

If
`ProjectSettings.display/window/subwindows/embed_subwindows<class_ProjectSettings_property_display/window/subwindows/embed_subwindows>`
is `true` (single-window mode), `rect`'s coordinates are global and
relative to the main window's top-left corner (excluding window
decorations). If `rect`'s position coordinates are negative, the window
will be located outside the main window and may not be visible as a
result.

If
`ProjectSettings.display/window/subwindows/embed_subwindows<class_ProjectSettings_property_display/window/subwindows/embed_subwindows>`
is `false` (multi-window mode), `rect`'s coordinates are global and
relative to the top-left corner of the leftmost screen. If `rect`'s
position coordinates are negative, the window will be placed at the
top-left corner of the screen.

\*\*Note:\*\* `rect` must be in global coordinates if specified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_centered**(minsize:
`Vector2i<class_Vector2i>` = Vector2i(0, 0))
`🔗<class_Window_method_popup_centered>`

Popups the **Window** at the center of the current screen, with
optionally given minimum size. If the **Window** is embedded, it will be
centered in the parent `Viewport<class_Viewport>` instead.

\*\*Note:\*\* Calling it with the default value of `minsize` is
equivalent to calling it with `size<class_Window_property_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_centered\_clamped**(minsize:
`Vector2i<class_Vector2i>` = Vector2i(0, 0), fallback\_ratio:
`float<class_float>` = 0.75)
`🔗<class_Window_method_popup_centered_clamped>`

Popups the **Window** centered inside its parent **Window**.
`fallback_ratio` determines the maximum size of the **Window**, in
relation to its parent.

\*\*Note:\*\* Calling it with the default value of `minsize` is
equivalent to calling it with `size<class_Window_property_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_centered\_ratio**(ratio:
`float<class_float>` = 0.8)
`🔗<class_Window_method_popup_centered_ratio>`

If **Window** is embedded, popups the **Window** centered inside its
embedder and sets its size as a `ratio` of embedder's size.

If **Window** is a native window, popups the **Window** centered inside
the screen of its parent **Window** and sets its size as a `ratio` of
the screen size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_exclusive**(from\_node:
`Node<class_Node>`, rect: `Rect2i<class_Rect2i>` = Rect2i(0, 0, 0, 0))
`🔗<class_Window_method_popup_exclusive>`

Attempts to parent this dialog to the last exclusive window relative to
`from_node`, and then calls `popup<class_Window_method_popup>` on it.
The dialog must have no current parent, otherwise the method fails.

See also
`set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`
and
`Node.get_last_exclusive_window<class_Node_method_get_last_exclusive_window>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_exclusive\_centered**(from\_node:
`Node<class_Node>`, minsize: `Vector2i<class_Vector2i>` = Vector2i(0,
0)) `🔗<class_Window_method_popup_exclusive_centered>`

Attempts to parent this dialog to the last exclusive window relative to
`from_node`, and then calls
`popup_centered<class_Window_method_popup_centered>` on it. The dialog
must have no current parent, otherwise the method fails.

See also
`set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`
and
`Node.get_last_exclusive_window<class_Node_method_get_last_exclusive_window>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**popup\_exclusive\_centered\_clamped**(from\_node: `Node<class_Node>`,
minsize: `Vector2i<class_Vector2i>` = Vector2i(0, 0), fallback\_ratio:
`float<class_float>` = 0.75)
`🔗<class_Window_method_popup_exclusive_centered_clamped>`

Attempts to parent this dialog to the last exclusive window relative to
`from_node`, and then calls
`popup_centered_clamped<class_Window_method_popup_centered_clamped>` on
it. The dialog must have no current parent, otherwise the method fails.

See also
`set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`
and
`Node.get_last_exclusive_window<class_Node_method_get_last_exclusive_window>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**popup\_exclusive\_centered\_ratio**(from\_node: `Node<class_Node>`,
ratio: `float<class_float>` = 0.8)
`🔗<class_Window_method_popup_exclusive_centered_ratio>`

Attempts to parent this dialog to the last exclusive window relative to
`from_node`, and then calls
`popup_centered_ratio<class_Window_method_popup_centered_ratio>` on it.
The dialog must have no current parent, otherwise the method fails.

See also
`set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`
and
`Node.get_last_exclusive_window<class_Node_method_get_last_exclusive_window>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_exclusive\_on\_parent**(from\_node:
`Node<class_Node>`, parent\_rect: `Rect2i<class_Rect2i>`)
`🔗<class_Window_method_popup_exclusive_on_parent>`

Attempts to parent this dialog to the last exclusive window relative to
`from_node`, and then calls
`popup_on_parent<class_Window_method_popup_on_parent>` on it. The dialog
must have no current parent, otherwise the method fails.

See also
`set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`
and
`Node.get_last_exclusive_window<class_Node_method_get_last_exclusive_window>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_on\_parent**(parent\_rect:
`Rect2i<class_Rect2i>`) `🔗<class_Window_method_popup_on_parent>`

Popups the **Window** with a position shifted by parent **Window**'s
position. If the **Window** is embedded, has the same effect as
`popup<class_Window_method_popup>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_color\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Window_method_remove_theme_color_override>`

Removes a local override for a theme `Color<class_Color>` with the
specified `name` previously added by
`add_theme_color_override<class_Window_method_add_theme_color_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_constant\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Window_method_remove_theme_constant_override>`

Removes a local override for a theme constant with the specified `name`
previously added by
`add_theme_constant_override<class_Window_method_add_theme_constant_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_font\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Window_method_remove_theme_font_override>`

Removes a local override for a theme `Font<class_Font>` with the
specified `name` previously added by
`add_theme_font_override<class_Window_method_add_theme_font_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_font\_size\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Window_method_remove_theme_font_size_override>`

Removes a local override for a theme font size with the specified `name`
previously added by
`add_theme_font_size_override<class_Window_method_add_theme_font_size_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_icon\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Window_method_remove_theme_icon_override>`

Removes a local override for a theme icon with the specified `name`
previously added by
`add_theme_icon_override<class_Window_method_add_theme_icon_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_stylebox\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Window_method_remove_theme_stylebox_override>`

Removes a local override for a theme `StyleBox<class_StyleBox>` with the
specified `name` previously added by
`add_theme_stylebox_override<class_Window_method_add_theme_stylebox_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **request\_attention**()
`🔗<class_Window_method_request_attention>`

Tells the OS that the **Window** needs an attention. This makes the
window stand out in some way depending on the system, e.g. it might
blink on the task bar.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset\_size**()
`🔗<class_Window_method_reset_size>`

Resets the size to the minimum size, which is the max of
`min_size<class_Window_property_min_size>` and (if
`wrap_controls<class_Window_property_wrap_controls>` is enabled)
`get_contents_minimum_size<class_Window_method_get_contents_minimum_size>`.
This is equivalent to calling `set_size(Vector2i())` (or any size below
the minimum).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_flag**(flag:
`Flags<enum_Window_Flags>`, enabled: `bool<class_bool>`)
`🔗<class_Window_method_set_flag>`

Sets a specified window flag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_ime\_active**(active:
`bool<class_bool>`) `🔗<class_Window_method_set_ime_active>`

If `active` is `true`, enables system's native IME (Input Method
Editor).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_ime\_position**(position:
`Vector2i<class_Vector2i>`) `🔗<class_Window_method_set_ime_position>`

Moves IME to the given position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layout\_direction**(direction:
`LayoutDirection<enum_Window_LayoutDirection>`)
`🔗<class_Window_method_set_layout_direction>`

Sets layout direction and text writing direction. Right-to-left layouts
are necessary for certain languages (e.g. Arabic and Hebrew).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_unparent\_when\_invisible**(unparent:
`bool<class_bool>`)
`🔗<class_Window_method_set_unparent_when_invisible>`

If `unparent` is `true`, the window is automatically unparented when
going invisible.

\*\*Note:\*\* Make sure to keep a reference to the node, otherwise it
will be orphaned. You also need to manually call
`Node.queue_free<class_Node_method_queue_free>` to free the window if
it's not parented.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_use\_font\_oversampling**(enable:
`bool<class_bool>`) `🔗<class_Window_method_set_use_font_oversampling>`

Enables font oversampling. This makes fonts look better when they are
scaled up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **show**() `🔗<class_Window_method_show>`

Makes the **Window** appear. This enables interactions with the
**Window** and doesn't change any of its property other than visibility
(unlike e.g. `popup<class_Window_method_popup>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **title\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_Window_theme_color_title_color>`

The color of the title's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **title\_outline\_modulate** = `Color(0, 0, 0, 1)`
`🔗<class_Window_theme_color_title_outline_modulate>`

The color of the title's text outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **close\_h\_offset** = `18`
`🔗<class_Window_theme_constant_close_h_offset>`

Horizontal position offset of the close button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **close\_v\_offset** = `24`
`🔗<class_Window_theme_constant_close_v_offset>`

Vertical position offset of the close button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **resize\_margin** = `4`
`🔗<class_Window_theme_constant_resize_margin>`

Defines the outside margin at which the window border can be grabbed
with mouse and resized.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **title\_height** = `36`
`🔗<class_Window_theme_constant_title_height>`

Height of the title bar.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **title\_outline\_size** = `0`
`🔗<class_Window_theme_constant_title_outline_size>`

The size of the title outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **title\_font**
`🔗<class_Window_theme_font_title_font>`

The font used to draw the title.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **title\_font\_size**
`🔗<class_Window_theme_font_size_title_font_size>`

The size of the title font.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **close**
`🔗<class_Window_theme_icon_close>`

The icon for the close button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **close\_pressed**
`🔗<class_Window_theme_icon_close_pressed>`

The icon for the close button when it's being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **embedded\_border**
`🔗<class_Window_theme_style_embedded_border>`

The background style used when the **Window** is embedded. Note that
this is drawn only under the window's content, excluding the title. For
proper borders and title bar style, you can use `expand_margin_*`
properties of `StyleBoxFlat<class_StyleBoxFlat>`.

\*\*Note:\*\* The content background will not be visible unless
`transparent<class_Window_property_transparent>` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **embedded\_unfocused\_border**
`🔗<class_Window_theme_style_embedded_unfocused_border>`

The background style used when the **Window** is embedded and unfocused.
