github\_url  
hide

# DisplayServer

**Inherits:** `Object<class_Object>`

A server interface for low-level window management.

classref-introduction-group

## Description

**DisplayServer** handles everything related to window management. It is
separated from `OS<class_OS>` as a single operating system may support
multiple display servers.

\*\*Headless mode:\*\* Starting the engine with the `--headless`
`command line argument <../tutorials/editor/command_line_tutorial>`
disables all rendering and window management functions. Most functions
from **DisplayServer** will return dummy values in this case.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Feature**: `🔗<enum_DisplayServer_Feature>`

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_GLOBAL\_MENU** = `0`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Display server supports global menu. This allows the application to
display its menu items in the operating system's top bar. **macOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_SUBWINDOWS** = `1`

Display server supports multiple windows that can be moved outside of
the main window. **Windows, macOS, Linux (X11)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_TOUCHSCREEN** = `2`

Display server supports touchscreen input. **Windows, Linux (X11),
Android, iOS, Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_MOUSE** = `3`

Display server supports mouse input. **Windows, macOS, Linux
(X11/Wayland), Android, Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_MOUSE\_WARP** = `4`

Display server supports warping mouse coordinates to keep the mouse
cursor constrained within an area, but looping when one of the edges is
reached. **Windows, macOS, Linux (X11/Wayland)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_CLIPBOARD** = `5`

Display server supports setting and getting clipboard data. See also
`FEATURE_CLIPBOARD_PRIMARY<class_DisplayServer_constant_FEATURE_CLIPBOARD_PRIMARY>`.
**Windows, macOS, Linux (X11/Wayland), Android, iOS, Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_VIRTUAL\_KEYBOARD** =
`6`

Display server supports popping up a virtual keyboard when requested to
input text without a physical keyboard. **Android, iOS, Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_CURSOR\_SHAPE** = `7`

Display server supports setting the mouse cursor shape to be different
from the default. **Windows, macOS, Linux (X11/Wayland), Android, Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_CUSTOM\_CURSOR\_SHAPE**
= `8`

Display server supports setting the mouse cursor shape to a custom
image. **Windows, macOS, Linux (X11/Wayland), Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_NATIVE\_DIALOG** = `9`

Display server supports spawning text dialogs using the operating
system's native look-and-feel. See
`dialog_show<class_DisplayServer_method_dialog_show>`. **Windows,
macOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_IME** = `10`

Display server supports [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method), which is commonly
used for inputting Chinese/Japanese/Korean text. This is handled by the
operating system, rather than by Godot. **Windows, macOS, Linux (X11)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_WINDOW\_TRANSPARENCY**
= `11`

Display server supports windows can use per-pixel transparency to make
windows behind them partially or fully visible. **Windows, macOS, Linux
(X11/Wayland)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_HIDPI** = `12`

Display server supports querying the operating system's display scale
factor. This allows for *reliable* automatic hiDPI display detection, as
opposed to guessing based on the screen resolution and reported display
DPI (which can be unreliable due to broken monitor EDID). **Windows,
Linux (Wayland), macOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_ICON** = `13`

Display server supports changing the window icon (usually displayed in
the top-left corner). **Windows, macOS, Linux (X11)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_NATIVE\_ICON** = `14`

Display server supports changing the window icon (usually displayed in
the top-left corner). **Windows, macOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_ORIENTATION** = `15`

Display server supports changing the screen orientation. **Android,
iOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_SWAP\_BUFFERS** = `16`

Display server supports V-Sync status can be changed from the default
(which is forced to be enabled platforms not supporting this feature).
**Windows, macOS, Linux (X11/Wayland)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_CLIPBOARD\_PRIMARY** =
`18`

Display server supports Primary clipboard can be used. This is a
different clipboard from
`FEATURE_CLIPBOARD<class_DisplayServer_constant_FEATURE_CLIPBOARD>`.
**Linux (X11/Wayland)**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_TEXT\_TO\_SPEECH** =
`19`

Display server supports text-to-speech. See `tts_*` methods. **Windows,
macOS, Linux (X11/Wayland), Android, iOS, Web**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_EXTEND\_TO\_TITLE** =
`20`

Display server supports expanding window content to the title. See
`WINDOW_FLAG_EXTEND_TO_TITLE<class_DisplayServer_constant_WINDOW_FLAG_EXTEND_TO_TITLE>`.
**macOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_SCREEN\_CAPTURE** =
`21`

Display server supports reading screen pixels. See
`screen_get_pixel<class_DisplayServer_method_screen_get_pixel>`.

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_STATUS\_INDICATOR** =
`22`

Display server supports application status indicators.

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_NATIVE\_HELP** = `23`

Display server supports native help system search callbacks. See
`help_set_search_callbacks<class_DisplayServer_method_help_set_search_callbacks>`.

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_NATIVE\_DIALOG\_INPUT**
= `24`

Display server supports spawning text input dialogs using the operating
system's native look-and-feel. See
`dialog_input_text<class_DisplayServer_method_dialog_input_text>`.
**Windows, macOS**

classref-enumeration-constant

`Feature<enum_DisplayServer_Feature>` **FEATURE\_NATIVE\_DIALOG\_FILE**
= `25`

Display server supports spawning dialogs for selecting files or
directories using the operating system's native look-and-feel. See
`file_dialog_show<class_DisplayServer_method_file_dialog_show>` and
`file_dialog_with_options_show<class_DisplayServer_method_file_dialog_with_options_show>`.
**Windows, macOS, Linux (X11/Wayland)**

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MouseMode**: `🔗<enum_DisplayServer_MouseMode>`

classref-enumeration-constant

`MouseMode<enum_DisplayServer_MouseMode>` **MOUSE\_MODE\_VISIBLE** = `0`

Makes the mouse cursor visible if it is hidden.

classref-enumeration-constant

`MouseMode<enum_DisplayServer_MouseMode>` **MOUSE\_MODE\_HIDDEN** = `1`

Makes the mouse cursor hidden if it is visible.

classref-enumeration-constant

`MouseMode<enum_DisplayServer_MouseMode>` **MOUSE\_MODE\_CAPTURED** =
`2`

Captures the mouse. The mouse will be hidden and its position locked at
the center of the window manager's window.

\*\*Note:\*\* If you want to process the mouse's movement in this mode,
you need to use
`InputEventMouseMotion.relative<class_InputEventMouseMotion_property_relative>`.

classref-enumeration-constant

`MouseMode<enum_DisplayServer_MouseMode>` **MOUSE\_MODE\_CONFINED** =
`3`

Confines the mouse cursor to the game window, and make it visible.

classref-enumeration-constant

`MouseMode<enum_DisplayServer_MouseMode>`
**MOUSE\_MODE\_CONFINED\_HIDDEN** = `4`

Confines the mouse cursor to the game window, and make it hidden.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ScreenOrientation**: `🔗<enum_DisplayServer_ScreenOrientation>`

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_LANDSCAPE** = `0`

Default landscape orientation.

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_PORTRAIT** = `1`

Default portrait orientation.

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_REVERSE\_LANDSCAPE** = `2`

Reverse landscape orientation (upside down).

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_REVERSE\_PORTRAIT** = `3`

Reverse portrait orientation (upside down).

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_SENSOR\_LANDSCAPE** = `4`

Automatic landscape orientation (default or reverse depending on
sensor).

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_SENSOR\_PORTRAIT** = `5`

Automatic portrait orientation (default or reverse depending on sensor).

classref-enumeration-constant

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**SCREEN\_SENSOR** = `6`

Automatic landscape or portrait orientation (default or reverse
depending on sensor).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VirtualKeyboardType**:
`🔗<enum_DisplayServer_VirtualKeyboardType>`

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_DEFAULT** = `0`

Default text virtual keyboard.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_MULTILINE** = `1`

Multiline virtual keyboard.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_NUMBER** = `2`

Virtual number keypad, useful for PIN entry.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_NUMBER\_DECIMAL** = `3`

Virtual number keypad, useful for entering fractional numbers.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_PHONE** = `4`

Virtual phone number keypad.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_EMAIL\_ADDRESS** = `5`

Virtual keyboard with additional keys to assist with typing email
addresses.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_PASSWORD** = `6`

Virtual keyboard for entering a password. On most platforms, this should
disable autocomplete and autocapitalization.

\*\*Note:\*\* This is not supported on Web. Instead, this behaves
identically to
`KEYBOARD_TYPE_DEFAULT<class_DisplayServer_constant_KEYBOARD_TYPE_DEFAULT>`.

classref-enumeration-constant

`VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
**KEYBOARD\_TYPE\_URL** = `7`

Virtual keyboard with additional keys to assist with typing URLs.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CursorShape**: `🔗<enum_DisplayServer_CursorShape>`

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_ARROW** = `0`

Arrow cursor shape. This is the default when not pointing anything that
overrides the mouse cursor, such as a `LineEdit<class_LineEdit>` or
`TextEdit<class_TextEdit>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_IBEAM** = `1`

I-beam cursor shape. This is used by default when hovering a control
that accepts text input, such as `LineEdit<class_LineEdit>` or
`TextEdit<class_TextEdit>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_POINTING\_HAND**
= `2`

Pointing hand cursor shape. This is used by default when hovering a
`LinkButton<class_LinkButton>` or a URL tag in a
`RichTextLabel<class_RichTextLabel>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_CROSS** = `3`

Crosshair cursor. This is intended to be displayed when the user needs
precise aim over an element, such as a rectangle selection tool or a
color picker.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_WAIT** = `4`

Wait cursor. On most cursor themes, this displays a spinning icon
*besides* the arrow. Intended to be used for non-blocking operations
(when the user can do something else at the moment). See also
`CURSOR_BUSY<class_DisplayServer_constant_CURSOR_BUSY>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_BUSY** = `5`

Wait cursor. On most cursor themes, this *replaces* the arrow with a
spinning icon. Intended to be used for blocking operations (when the
user can't do anything else at the moment). See also
`CURSOR_WAIT<class_DisplayServer_constant_CURSOR_WAIT>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_DRAG** = `6`

Dragging hand cursor. This is displayed during drag-and-drop operations.
See also
`CURSOR_CAN_DROP<class_DisplayServer_constant_CURSOR_CAN_DROP>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_CAN\_DROP** =
`7`

"Can drop" cursor. This is displayed during drag-and-drop operations if
hovering over a `Control<class_Control>` that can accept the
drag-and-drop event. On most cursor themes, this displays a dragging
hand with an arrow symbol besides it. See also
`CURSOR_DRAG<class_DisplayServer_constant_CURSOR_DRAG>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_FORBIDDEN** =
`8`

Forbidden cursor. This is displayed during drag-and-drop operations if
the hovered `Control<class_Control>` can't accept the drag-and-drop
event.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_VSIZE** = `9`

Vertical resize cursor. Intended to be displayed when the hovered
`Control<class_Control>` can be vertically resized using the mouse. See
also `CURSOR_VSPLIT<class_DisplayServer_constant_CURSOR_VSPLIT>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_HSIZE** = `10`

Horizontal resize cursor. Intended to be displayed when the hovered
`Control<class_Control>` can be horizontally resized using the mouse.
See also `CURSOR_HSPLIT<class_DisplayServer_constant_CURSOR_HSPLIT>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_BDIAGSIZE** =
`11`

Secondary diagonal resize cursor (top-right/bottom-left). Intended to be
displayed when the hovered `Control<class_Control>` can be resized on
both axes at once using the mouse.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_FDIAGSIZE** =
`12`

Main diagonal resize cursor (top-left/bottom-right). Intended to be
displayed when the hovered `Control<class_Control>` can be resized on
both axes at once using the mouse.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_MOVE** = `13`

Move cursor. Intended to be displayed when the hovered
`Control<class_Control>` can be moved using the mouse.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_VSPLIT** = `14`

Vertical split cursor. This is displayed when hovering a
`Control<class_Control>` with splits that can be vertically resized
using the mouse, such as `VSplitContainer<class_VSplitContainer>`. On
some cursor themes, this cursor may have the same appearance as
`CURSOR_VSIZE<class_DisplayServer_constant_CURSOR_VSIZE>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_HSPLIT** = `15`

Horizontal split cursor. This is displayed when hovering a
`Control<class_Control>` with splits that can be horizontally resized
using the mouse, such as `HSplitContainer<class_HSplitContainer>`. On
some cursor themes, this cursor may have the same appearance as
`CURSOR_HSIZE<class_DisplayServer_constant_CURSOR_HSIZE>`.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_HELP** = `16`

Help cursor. On most cursor themes, this displays a question mark icon
instead of the mouse cursor. Intended to be used when the user has
requested help on the next element that will be clicked.

classref-enumeration-constant

`CursorShape<enum_DisplayServer_CursorShape>` **CURSOR\_MAX** = `17`

Represents the size of the `CursorShape<enum_DisplayServer_CursorShape>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FileDialogMode**: `🔗<enum_DisplayServer_FileDialogMode>`

classref-enumeration-constant

`FileDialogMode<enum_DisplayServer_FileDialogMode>`
**FILE\_DIALOG\_MODE\_OPEN\_FILE** = `0`

The native file dialog allows selecting one, and only one file.

classref-enumeration-constant

`FileDialogMode<enum_DisplayServer_FileDialogMode>`
**FILE\_DIALOG\_MODE\_OPEN\_FILES** = `1`

The native file dialog allows selecting multiple files.

classref-enumeration-constant

`FileDialogMode<enum_DisplayServer_FileDialogMode>`
**FILE\_DIALOG\_MODE\_OPEN\_DIR** = `2`

The native file dialog only allows selecting a directory, disallowing
the selection of any file.

classref-enumeration-constant

`FileDialogMode<enum_DisplayServer_FileDialogMode>`
**FILE\_DIALOG\_MODE\_OPEN\_ANY** = `3`

The native file dialog allows selecting one file or directory.

classref-enumeration-constant

`FileDialogMode<enum_DisplayServer_FileDialogMode>`
**FILE\_DIALOG\_MODE\_SAVE\_FILE** = `4`

The native file dialog will warn when a file exists.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **WindowMode**: `🔗<enum_DisplayServer_WindowMode>`

classref-enumeration-constant

`WindowMode<enum_DisplayServer_WindowMode>` **WINDOW\_MODE\_WINDOWED** =
`0`

Windowed mode, i.e. `Window<class_Window>` doesn't occupy the whole
screen (unless set to the size of the screen).

classref-enumeration-constant

`WindowMode<enum_DisplayServer_WindowMode>` **WINDOW\_MODE\_MINIMIZED**
= `1`

Minimized window mode, i.e. `Window<class_Window>` is not visible and
available on window manager's window list. Normally happens when the
minimize button is pressed.

classref-enumeration-constant

`WindowMode<enum_DisplayServer_WindowMode>` **WINDOW\_MODE\_MAXIMIZED**
= `2`

Maximized window mode, i.e. `Window<class_Window>` will occupy whole
screen area except task bar and still display its borders. Normally
happens when the maximize button is pressed.

classref-enumeration-constant

`WindowMode<enum_DisplayServer_WindowMode>` **WINDOW\_MODE\_FULLSCREEN**
= `3`

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

`WindowMode<enum_DisplayServer_WindowMode>`
**WINDOW\_MODE\_EXCLUSIVE\_FULLSCREEN** = `4`

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

enum **WindowFlags**: `🔗<enum_DisplayServer_WindowFlags>`

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_RESIZE\_DISABLED** = `0`

The window can't be resized by dragging its resize grip. It's still
possible to resize the window using
`window_set_size<class_DisplayServer_method_window_set_size>`. This flag
is ignored for full screen windows.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_BORDERLESS** = `1`

The window do not have native title bar and other decorations. This flag
is ignored for full-screen windows.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_ALWAYS\_ON\_TOP** = `2`

The window is floating on top of all other windows. This flag is ignored
for full-screen windows.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_TRANSPARENT** = `3`

The window background can be transparent.

\*\*Note:\*\* This flag has no effect if
`is_window_transparency_available<class_DisplayServer_method_is_window_transparency_available>`
returns `false`.

\*\*Note:\*\* Transparency support is implemented on Linux
(X11/Wayland), macOS, and Windows, but availability might vary depending
on GPU driver, display manager, and compositor capabilities.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_NO\_FOCUS** = `4`

The window can't be focused. No-focus window will ignore all input,
except mouse clicks.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>` **WINDOW\_FLAG\_POPUP** =
`5`

Window is part of menu or `OptionButton<class_OptionButton>` dropdown.
This flag can't be changed when the window is visible. An active popup
window will exclusively receive all input, without stealing focus from
its parent. Popup windows are automatically closed when uses click
outside it, or when an application is switched. Popup window must have
transient parent set (see
`window_set_transient<class_DisplayServer_method_window_set_transient>`).

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_EXTEND\_TO\_TITLE** = `6`

Window content is expanded to the full size of the window. Unlike
borderless window, the frame is left intact and can be used to resize
the window, title bar is transparent, but have minimize/maximize/close
buttons.

Use
`window_set_window_buttons_offset<class_DisplayServer_method_window_set_window_buttons_offset>`
to adjust minimize/maximize/close buttons offset.

Use
`window_get_safe_title_margins<class_DisplayServer_method_window_get_safe_title_margins>`
to determine area under the title bar that is not covered by
decorations.

\*\*Note:\*\* This flag is implemented only on macOS.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>`
**WINDOW\_FLAG\_MOUSE\_PASSTHROUGH** = `7`

All mouse events are passed to the underlying window of the same
application.

classref-enumeration-constant

`WindowFlags<enum_DisplayServer_WindowFlags>` **WINDOW\_FLAG\_MAX** =
`8`

Max value of the `WindowFlags<enum_DisplayServer_WindowFlags>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **WindowEvent**: `🔗<enum_DisplayServer_WindowEvent>`

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_MOUSE\_ENTER** = `0`

Sent when the mouse pointer enters the window.

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_MOUSE\_EXIT** = `1`

Sent when the mouse pointer exits the window.

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_FOCUS\_IN** = `2`

Sent when the window grabs focus.

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_FOCUS\_OUT** = `3`

Sent when the window loses focus.

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_CLOSE\_REQUEST** = `4`

Sent when the user has attempted to close the window (e.g. close button
is pressed).

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_GO\_BACK\_REQUEST** = `5`

Sent when the device "Back" button is pressed.

\*\*Note:\*\* This event is implemented only on Android.

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_DPI\_CHANGE** = `6`

Sent when the window is moved to the display with different DPI, or
display DPI is changed.

\*\*Note:\*\* This flag is implemented only on macOS.

classref-enumeration-constant

`WindowEvent<enum_DisplayServer_WindowEvent>`
**WINDOW\_EVENT\_TITLEBAR\_CHANGE** = `7`

Sent when the window title bar decoration is changed (e.g.
`WINDOW_FLAG_EXTEND_TO_TITLE<class_DisplayServer_constant_WINDOW_FLAG_EXTEND_TO_TITLE>`
is set or window entered/exited full screen mode).

\*\*Note:\*\* This flag is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VSyncMode**: `🔗<enum_DisplayServer_VSyncMode>`

classref-enumeration-constant

`VSyncMode<enum_DisplayServer_VSyncMode>` **VSYNC\_DISABLED** = `0`

No vertical synchronization, which means the engine will display frames
as fast as possible (tearing may be visible). Framerate is unlimited
(regardless of `Engine.max_fps<class_Engine_property_max_fps>`).

classref-enumeration-constant

`VSyncMode<enum_DisplayServer_VSyncMode>` **VSYNC\_ENABLED** = `1`

Default vertical synchronization mode, the image is displayed only on
vertical blanking intervals (no tearing is visible). Framerate is
limited by the monitor refresh rate (regardless of
`Engine.max_fps<class_Engine_property_max_fps>`).

classref-enumeration-constant

`VSyncMode<enum_DisplayServer_VSyncMode>` **VSYNC\_ADAPTIVE** = `2`

Behaves like
`VSYNC_DISABLED<class_DisplayServer_constant_VSYNC_DISABLED>` when the
framerate drops below the screen's refresh rate to reduce stuttering
(tearing may be visible). Otherwise, vertical synchronization is enabled
to avoid tearing. Framerate is limited by the monitor refresh rate
(regardless of `Engine.max_fps<class_Engine_property_max_fps>`). Behaves
like `VSYNC_ENABLED<class_DisplayServer_constant_VSYNC_ENABLED>` when
using the Compatibility rendering method.

classref-enumeration-constant

`VSyncMode<enum_DisplayServer_VSyncMode>` **VSYNC\_MAILBOX** = `3`

Displays the most recent image in the queue on vertical blanking
intervals, while rendering to the other images (no tearing is visible).
Framerate is unlimited (regardless of
`Engine.max_fps<class_Engine_property_max_fps>`).

Although not guaranteed, the images can be rendered as fast as possible,
which may reduce input lag (also called "Fast" V-Sync mode).
`VSYNC_MAILBOX<class_DisplayServer_constant_VSYNC_MAILBOX>` works best
when at least twice as many frames as the display refresh rate are
rendered. Behaves like
`VSYNC_ENABLED<class_DisplayServer_constant_VSYNC_ENABLED>` when using
the Compatibility rendering method.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **HandleType**: `🔗<enum_DisplayServer_HandleType>`

classref-enumeration-constant

`HandleType<enum_DisplayServer_HandleType>` **DISPLAY\_HANDLE** = `0`

Display handle:

-   Linux (X11): `X11::Display*` for the display.
-   Android: `EGLDisplay` for the display.

classref-enumeration-constant

`HandleType<enum_DisplayServer_HandleType>` **WINDOW\_HANDLE** = `1`

Window handle:

-   Windows: `HWND` for the window.
-   Linux (X11): `X11::Window*` for the window.
-   macOS: `NSWindow*` for the window.
-   iOS: `UIViewController*` for the view controller.
-   Android: `jObject` for the activity.

classref-enumeration-constant

`HandleType<enum_DisplayServer_HandleType>` **WINDOW\_VIEW** = `2`

Window view:

-   Windows: `HDC` for the window (only with the GL Compatibility
    renderer).
-   macOS: `NSView*` for the window main view.
-   iOS: `UIView*` for the window main view.

classref-enumeration-constant

`HandleType<enum_DisplayServer_HandleType>` **OPENGL\_CONTEXT** = `3`

OpenGL context (only with the GL Compatibility renderer):

-   Windows: `HGLRC` for the window (native GL), or `EGLContext` for the
    window (ANGLE).
-   Linux (X11): `GLXContext*` for the window.
-   macOS: `NSOpenGLContext*` for the window (native GL), or
    `EGLContext` for the window (ANGLE).
-   Android: `EGLContext` for the window.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TTSUtteranceEvent**: `🔗<enum_DisplayServer_TTSUtteranceEvent>`

classref-enumeration-constant

`TTSUtteranceEvent<enum_DisplayServer_TTSUtteranceEvent>`
**TTS\_UTTERANCE\_STARTED** = `0`

Utterance has begun to be spoken.

classref-enumeration-constant

`TTSUtteranceEvent<enum_DisplayServer_TTSUtteranceEvent>`
**TTS\_UTTERANCE\_ENDED** = `1`

Utterance was successfully finished.

classref-enumeration-constant

`TTSUtteranceEvent<enum_DisplayServer_TTSUtteranceEvent>`
**TTS\_UTTERANCE\_CANCELED** = `2`

Utterance was canceled, or TTS service was unable to process it.

classref-enumeration-constant

`TTSUtteranceEvent<enum_DisplayServer_TTSUtteranceEvent>`
**TTS\_UTTERANCE\_BOUNDARY** = `3`

Utterance reached a word or sentence boundary.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**SCREEN\_WITH\_MOUSE\_FOCUS** = `-4`
`🔗<class_DisplayServer_constant_SCREEN_WITH_MOUSE_FOCUS>`

Represents the screen containing the mouse pointer.

\*\*Note:\*\* On Linux (Wayland), this constant always represents the
screen at index `0`.

classref-constant

**SCREEN\_WITH\_KEYBOARD\_FOCUS** = `-3`
`🔗<class_DisplayServer_constant_SCREEN_WITH_KEYBOARD_FOCUS>`

Represents the screen containing the window with the keyboard focus.

\*\*Note:\*\* On Linux (Wayland), this constant always represents the
screen at index `0`.

classref-constant

**SCREEN\_PRIMARY** = `-2`
`🔗<class_DisplayServer_constant_SCREEN_PRIMARY>`

Represents the primary screen.

\*\*Note:\*\* On Linux (Wayland), this constant always represents the
screen at index `0`.

classref-constant

**SCREEN\_OF\_MAIN\_WINDOW** = `-1`
`🔗<class_DisplayServer_constant_SCREEN_OF_MAIN_WINDOW>`

Represents the screen where the main window is located. This is usually
the default value in functions that allow specifying one of several
screens.

\*\*Note:\*\* On Linux (Wayland), this constant always represents the
screen at index `0`.

classref-constant

**MAIN\_WINDOW\_ID** = `0`
`🔗<class_DisplayServer_constant_MAIN_WINDOW_ID>`

The ID of the main window spawned by the engine, which can be passed to
methods expecting a `window_id`.

classref-constant

**INVALID\_WINDOW\_ID** = `-1`
`🔗<class_DisplayServer_constant_INVALID_WINDOW_ID>`

The ID that refers to a nonexistent window. This is returned by some
**DisplayServer** methods if no window matches the requested result.

classref-constant

**INVALID\_INDICATOR\_ID** = `-1`
`🔗<class_DisplayServer_constant_INVALID_INDICATOR_ID>`

The ID that refers to a nonexistent application status indicator.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **clipboard\_get**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_clipboard_get>`

Returns the user's clipboard as a string if possible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **clipboard\_get\_image**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_clipboard_get_image>`

Returns the user's clipboard as an image if possible.

\*\*Note:\*\* This method uses the copied pixel data, e.g. from a image
editing software or a web browser, not an image file copied from file
explorer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **clipboard\_get\_primary**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_clipboard_get_primary>`

Returns the user's
[primary](https://unix.stackexchange.com/questions/139191/whats-the-difference-between-primary-selection-and-clipboard-buffer)
clipboard as a string if possible. This is the clipboard that is set
when the user selects text in any application, rather than when pressing
`Ctrl + C`. The clipboard data can then be pasted by clicking the middle
mouse button in any application that supports the primary clipboard
mechanism.

\*\*Note:\*\* This method is only implemented on Linux (X11/Wayland).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **clipboard\_has**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_clipboard_has>`

Returns `true` if there is a text content on the user's clipboard.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **clipboard\_has\_image**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_clipboard_has_image>`

Returns `true` if there is an image content on the user's clipboard.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clipboard\_set**(clipboard:
`String<class_String>`) `🔗<class_DisplayServer_method_clipboard_set>`

Sets the user's clipboard content to the given string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**clipboard\_set\_primary**(clipboard\_primary: `String<class_String>`)
`🔗<class_DisplayServer_method_clipboard_set_primary>`

Sets the user's
[primary](https://unix.stackexchange.com/questions/139191/whats-the-difference-between-primary-selection-and-clipboard-buffer)
clipboard content to the given string. This is the clipboard that is set
when the user selects text in any application, rather than when pressing
`Ctrl + C`. The clipboard data can then be pasted by clicking the middle
mouse button in any application that supports the primary clipboard
mechanism.

\*\*Note:\*\* This method is only implemented on Linux (X11/Wayland).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **create\_status\_indicator**(icon:
`Texture2D<class_Texture2D>`, tooltip: `String<class_String>`, callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_create_status_indicator>`

Creates a new application status indicator with the specified icon,
tooltip, and activation callback.

`callback` should take two arguments: the pressed mouse button (one of
the `MouseButton<enum_@GlobalScope_MouseButton>` constants) and the
click position in screen coordinates (a `Vector2i<class_Vector2i>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`CursorShape<enum_DisplayServer_CursorShape>` **cursor\_get\_shape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_cursor_get_shape>`

Returns the default mouse cursor shape set by
`cursor_set_shape<class_DisplayServer_method_cursor_set_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cursor\_set\_custom\_image**(cursor:
`Resource<class_Resource>`, shape:
`CursorShape<enum_DisplayServer_CursorShape>` = 0, hotspot:
`Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_DisplayServer_method_cursor_set_custom_image>`

Sets a custom mouse cursor image for the given `shape`. This means the
user's operating system and mouse cursor theme will no longer influence
the mouse cursor's appearance.

`cursor` can be either a `Texture2D<class_Texture2D>` or an
`Image<class_Image>`, and it should not be larger than 256×256 to
display correctly. Optionally, `hotspot` can be set to offset the
image's position relative to the click point. By default, `hotspot` is
set to the top-left corner of the image. See also
`cursor_set_shape<class_DisplayServer_method_cursor_set_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cursor\_set\_shape**(shape:
`CursorShape<enum_DisplayServer_CursorShape>`)
`🔗<class_DisplayServer_method_cursor_set_shape>`

Sets the default mouse cursor shape. The cursor's appearance will vary
depending on the user's operating system and mouse cursor theme. See
also `cursor_get_shape<class_DisplayServer_method_cursor_get_shape>` and
`cursor_set_custom_image<class_DisplayServer_method_cursor_set_custom_image>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **delete\_status\_indicator**(id:
`int<class_int>`)
`🔗<class_DisplayServer_method_delete_status_indicator>`

Removes the application status indicator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **dialog\_input\_text**(title:
`String<class_String>`, description: `String<class_String>`,
existing\_text: `String<class_String>`, callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_dialog_input_text>`

Shows a text input dialog which uses the operating system's native
look-and-feel. `callback` should accept a single `String<class_String>`
parameter which contains the text field's contents.

\*\*Note:\*\* This method is implemented if the display server has the
`FEATURE_NATIVE_DIALOG_INPUT<class_DisplayServer_constant_FEATURE_NATIVE_DIALOG_INPUT>`
feature. Supported platforms include macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **dialog\_show**(title:
`String<class_String>`, description: `String<class_String>`, buttons:
`PackedStringArray<class_PackedStringArray>`, callback:
`Callable<class_Callable>`) `🔗<class_DisplayServer_method_dialog_show>`

Shows a text dialog which uses the operating system's native
look-and-feel. `callback` should accept a single `int<class_int>`
parameter which corresponds to the index of the pressed button.

\*\*Note:\*\* This method is implemented if the display server has the
`FEATURE_NATIVE_DIALOG<class_DisplayServer_constant_FEATURE_NATIVE_DIALOG>`
feature. Supported platforms include macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **enable\_for\_stealing\_focus**(process\_id:
`int<class_int>`)
`🔗<class_DisplayServer_method_enable_for_stealing_focus>`

Allows the `process_id` PID to steal focus from this window. In other
words, this disables the operating system's focus stealing protection
for the specified PID.

\*\*Note:\*\* This method is implemented only on Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **file\_dialog\_show**(title:
`String<class_String>`, current\_directory: `String<class_String>`,
filename: `String<class_String>`, show\_hidden: `bool<class_bool>`,
mode: `FileDialogMode<enum_DisplayServer_FileDialogMode>`, filters:
`PackedStringArray<class_PackedStringArray>`, callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_file_dialog_show>`

Displays OS native dialog for selecting files or directories in the file
system.

Each filter string in the `filters` array should be formatted like this:
`*.txt,*.doc;Text Files`. The description text of the filter is optional
and can be omitted. See also
`FileDialog.filters<class_FileDialog_property_filters>`.

Callbacks have the following arguments:
`status: bool, selected_paths: PackedStringArray, selected_filter_index: int`.

\*\*Note:\*\* This method is implemented if the display server has the
`FEATURE_NATIVE_DIALOG_FILE<class_DisplayServer_constant_FEATURE_NATIVE_DIALOG_FILE>`
feature. Supported platforms include Linux (X11/Wayland), Windows, and
macOS.

\*\*Note:\*\* `current_directory` might be ignored.

\*\*Note:\*\* On Linux, `show_hidden` is ignored.

\*\*Note:\*\* On macOS, native file dialogs have no title.

\*\*Note:\*\* On macOS, sandboxed apps will save security-scoped
bookmarks to retain access to the opened folders across multiple
sessions. Use
`OS.get_granted_permissions<class_OS_method_get_granted_permissions>` to
get a list of saved bookmarks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**file\_dialog\_with\_options\_show**(title: `String<class_String>`,
current\_directory: `String<class_String>`, root:
`String<class_String>`, filename: `String<class_String>`, show\_hidden:
`bool<class_bool>`, mode:
`FileDialogMode<enum_DisplayServer_FileDialogMode>`, filters:
`PackedStringArray<class_PackedStringArray>`, options:
`Array<class_Array>`\[`Dictionary<class_Dictionary>`\], callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_file_dialog_with_options_show>`

Displays OS native dialog for selecting files or directories in the file
system with additional user selectable options.

Each filter string in the `filters` array should be formatted like this:
`*.txt,*.doc;Text Files`. The description text of the filter is optional
and can be omitted. See also
`FileDialog.filters<class_FileDialog_property_filters>`.

`options` is array of `Dictionary<class_Dictionary>`s with the following
keys:

-   `"name"` - option's name `String<class_String>`.
-   `"values"` - `PackedStringArray<class_PackedStringArray>` of values.
    If empty, boolean option (check box) is used.
-   `"default"` - default selected option index (`int<class_int>`) or
    default boolean value (`bool<class_bool>`).

Callbacks have the following arguments:
`status: bool, selected_paths: PackedStringArray, selected_filter_index: int, selected_option: Dictionary`.

\*\*Note:\*\* This method is implemented if the display server has the
`FEATURE_NATIVE_DIALOG_FILE<class_DisplayServer_constant_FEATURE_NATIVE_DIALOG_FILE>`
feature. Supported platforms include Linux (X11/Wayland), Windows, and
macOS.

\*\*Note:\*\* `current_directory` might be ignored.

\*\*Note:\*\* On Linux (X11), `show_hidden` is ignored.

\*\*Note:\*\* On macOS, native file dialogs have no title.

\*\*Note:\*\* On macOS, sandboxed apps will save security-scoped
bookmarks to retain access to the opened folders across multiple
sessions. Use
`OS.get_granted_permissions<class_OS_method_get_granted_permissions>` to
get a list of saved bookmarks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_process\_and\_drop\_events**()
`🔗<class_DisplayServer_method_force_process_and_drop_events>`

Forces window manager processing while ignoring all
`InputEvent<class_InputEvent>`s. See also
`process_events<class_DisplayServer_method_process_events>`.

\*\*Note:\*\* This method is implemented on Windows and macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_accent\_color**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_accent_color>`

Returns OS theme accent color. Returns `Color(0, 0, 0, 0)`, if accent
color is unknown.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_base\_color**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_base_color>`

Returns the OS theme base color (default control background). Returns
`Color(0, 0, 0, 0)` if the base color is unknown.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Rect2<class_Rect2>`\] **get\_display\_cutouts**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_display_cutouts>`

Returns an `Array<class_Array>` of `Rect2<class_Rect2>`, each of which
is the bounding rectangle for a display cutout or notch. These are
non-functional areas on edge-to-edge screens used by cameras and
sensors. Returns an empty array if the device does not have cutouts. See
also
`get_display_safe_area<class_DisplayServer_method_get_display_safe_area>`.

\*\*Note:\*\* Currently only implemented on Android. Other platforms
will return an empty array even if they do have display cutouts or
notches.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **get\_display\_safe\_area**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_display_safe_area>`

Returns the unobscured area of the display where interactive controls
should be rendered. See also
`get_display_cutouts<class_DisplayServer_method_get_display_cutouts>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_keyboard\_focus\_screen**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_keyboard_focus_screen>`

Returns the index of the screen containing the window with the keyboard
focus, or the primary screen if there's no focused window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_name>`

Returns the name of the **DisplayServer** currently in use. Most
operating systems only have a single **DisplayServer**, but Linux has
access to more than one **DisplayServer** (currently X11 and Wayland).

The names of built-in display servers are `Windows`, `macOS`, `X11`
(Linux), `Wayland` (Linux), `Android`, `iOS`, `web` (HTML5), and
`headless` (when started with the `--headless`
`command line argument <../tutorials/editor/command_line_tutorial>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_primary\_screen**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_primary_screen>`

Returns index of the primary screen.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_screen\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_screen_count>`

Returns the number of displays available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_screen\_from\_rect**(rect: `Rect2<class_Rect2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_screen_from_rect>`

Returns index of the screen which contains specified rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_swap\_cancel\_ok**()
`🔗<class_DisplayServer_method_get_swap_cancel_ok>`

Returns `true` if positions of **OK** and **Cancel** buttons are swapped
in dialogs. This is enabled by default on Windows to follow interface
conventions, and be toggled by changing
`ProjectSettings.gui/common/swap_cancel_ok<class_ProjectSettings_property_gui/common/swap_cancel_ok>`.

\*\*Note:\*\* This doesn't affect native dialogs such as the ones
spawned by `dialog_show<class_DisplayServer_method_dialog_show>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_window\_at\_screen\_position**(position:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_window_at_screen_position>`

Returns the ID of the window at the specified screen `position` (in
pixels). On multi-monitor setups, the screen position is relative to the
virtual desktop area. On multi-monitor setups with different screen
resolutions or orientations, the origin may be located outside any
display like this:

    * (0, 0)        +-------+
                    |       |
    +-------------+ |       |
    |             | |       |
    |             | |       |
    +-------------+ +-------+

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_window\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_get_window_list>`

Returns the list of Godot window IDs belonging to this process.

\*\*Note:\*\* Native dialogs are not included in this list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_check\_item**(menu\_root:
`String<class_String>`, label: `String<class_String>`, callback:
`Callable<class_Callable>` = Callable(), key\_callback:
`Callable<class_Callable>` = Callable(), tag: `Variant<class_Variant>` =
null, accelerator: `Key<enum_@GlobalScope_Key>` = 0, index:
`int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_check_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new checkable item with text `label` to the global menu with ID
`menu_root`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_icon\_check\_item**(menu\_root:
`String<class_String>`, icon: `Texture2D<class_Texture2D>`, label:
`String<class_String>`, callback: `Callable<class_Callable>` =
Callable(), key\_callback: `Callable<class_Callable>` = Callable(), tag:
`Variant<class_Variant>` = null, accelerator:
`Key<enum_@GlobalScope_Key>` = 0, index: `int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_icon_check_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new checkable item with text `label` and icon `icon` to the
global menu with ID `menu_root`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_icon\_item**(menu\_root:
`String<class_String>`, icon: `Texture2D<class_Texture2D>`, label:
`String<class_String>`, callback: `Callable<class_Callable>` =
Callable(), key\_callback: `Callable<class_Callable>` = Callable(), tag:
`Variant<class_Variant>` = null, accelerator:
`Key<enum_@GlobalScope_Key>` = 0, index: `int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_icon_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new item with text `label` and icon `icon` to the global menu
with ID `menu_root`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**global\_menu\_add\_icon\_radio\_check\_item**(menu\_root:
`String<class_String>`, icon: `Texture2D<class_Texture2D>`, label:
`String<class_String>`, callback: `Callable<class_Callable>` =
Callable(), key\_callback: `Callable<class_Callable>` = Callable(), tag:
`Variant<class_Variant>` = null, accelerator:
`Key<enum_@GlobalScope_Key>` = 0, index: `int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_icon_radio_check_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new radio-checkable item with text `label` and icon `icon` to the
global menu with ID `menu_root`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* Radio-checkable items just display a checkmark, but don't
have any built-in checking behavior and must be checked/unchecked
manually. See
`global_menu_set_item_checked<class_DisplayServer_method_global_menu_set_item_checked>`
for more info on how to control it.

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_item**(menu\_root:
`String<class_String>`, label: `String<class_String>`, callback:
`Callable<class_Callable>` = Callable(), key\_callback:
`Callable<class_Callable>` = Callable(), tag: `Variant<class_Variant>` =
null, accelerator: `Key<enum_@GlobalScope_Key>` = 0, index:
`int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new item with text `label` to the global menu with ID
`menu_root`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_multistate\_item**(menu\_root:
`String<class_String>`, label: `String<class_String>`, max\_states:
`int<class_int>`, default\_state: `int<class_int>`, callback:
`Callable<class_Callable>` = Callable(), key\_callback:
`Callable<class_Callable>` = Callable(), tag: `Variant<class_Variant>` =
null, accelerator: `Key<enum_@GlobalScope_Key>` = 0, index:
`int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_multistate_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new item with text `label` to the global menu with ID
`menu_root`.

Contrarily to normal binary items, multistate items can have more than
two states, as defined by `max_states`. Each press or activate of the
item will increase the state by one. The default value is defined by
`default_state`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* By default, there's no indication of the current item
state, it should be changed manually.

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_radio\_check\_item**(menu\_root:
`String<class_String>`, label: `String<class_String>`, callback:
`Callable<class_Callable>` = Callable(), key\_callback:
`Callable<class_Callable>` = Callable(), tag: `Variant<class_Variant>` =
null, accelerator: `Key<enum_@GlobalScope_Key>` = 0, index:
`int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_radio_check_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a new radio-checkable item with text `label` to the global menu
with ID `menu_root`.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

An `accelerator` can optionally be defined, which is a keyboard shortcut
that can be pressed to trigger the menu button even if it's not
currently open. The `accelerator` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* Radio-checkable items just display a checkmark, but don't
have any built-in checking behavior and must be checked/unchecked
manually. See
`global_menu_set_item_checked<class_DisplayServer_method_global_menu_set_item_checked>`
for more info on how to control it.

\*\*Note:\*\* The `callback` and `key_callback` Callables need to accept
exactly one Variant parameter, the parameter passed to the Callables
will be the value passed to `tag`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_separator**(menu\_root:
`String<class_String>`, index: `int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_separator>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds a separator between items to the global menu with ID `menu_root`.
Separators also occupy an index.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_add\_submenu\_item**(menu\_root:
`String<class_String>`, label: `String<class_String>`, submenu:
`String<class_String>`, index: `int<class_int>` = -1)
`🔗<class_DisplayServer_method_global_menu_add_submenu_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Adds an item that will act as a submenu of the global menu `menu_root`.
The `submenu` argument is the ID of the global menu root that will be
shown when the item is clicked.

Returns index of the inserted item, it's not guaranteed to be the same
as `index` value.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_menu\_clear**(menu\_root:
`String<class_String>`)
`🔗<class_DisplayServer_method_global_menu_clear>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Removes all items from the global menu with ID `menu_root`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Supported system menu IDs:\*\*

    "_main" - Main menu (macOS).
    "_dock" - Dock popup menu (macOS).
    "_apple" - Apple menu (macOS, custom items added before "Services").
    "_window" - Window menu (macOS, custom items added after "Bring All to Front").
    "_help" - Help menu (macOS).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>`
**global\_menu\_get\_item\_accelerator**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_accelerator>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the accelerator of the item at index `idx`. Accelerators are
special combinations of keys that activate the item, no matter which
control is focused.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Callable<class_Callable>`
**global\_menu\_get\_item\_callback**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_callback>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the callback of the item at index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_get\_item\_count**(menu\_root:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_count>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns number of items in the global menu with ID `menu_root`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>`
**global\_menu\_get\_item\_icon**(menu\_root: `String<class_String>`,
idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_icon>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the icon of the item at index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**global\_menu\_get\_item\_indentation\_level**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_indentation_level>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the horizontal offset of the item at the given `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**global\_menu\_get\_item\_index\_from\_tag**(menu\_root:
`String<class_String>`, tag: `Variant<class_Variant>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_index_from_tag>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the index of the item with the specified `tag`. Indices are
automatically assigned to each item by the engine, and cannot be set
manually.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**global\_menu\_get\_item\_index\_from\_text**(menu\_root:
`String<class_String>`, text: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_index_from_text>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the index of the item with the specified `text`. Indices are
automatically assigned to each item by the engine, and cannot be set
manually.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Callable<class_Callable>`
**global\_menu\_get\_item\_key\_callback**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_key_callback>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the callback of the item accelerator at index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_get\_item\_max\_states**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_max_states>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns number of states of a multistate item. See
`global_menu_add_multistate_item<class_DisplayServer_method_global_menu_add_multistate_item>`
for details.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **global\_menu\_get\_item\_state**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_state>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the state of a multistate item. See
`global_menu_add_multistate_item<class_DisplayServer_method_global_menu_add_multistate_item>`
for details.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **global\_menu\_get\_item\_submenu**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_submenu>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the submenu ID of the item at index `idx`. See
`global_menu_add_submenu_item<class_DisplayServer_method_global_menu_add_submenu_item>`
for more info on how to add a submenu.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **global\_menu\_get\_item\_tag**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_tag>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the metadata of the specified item, which might be of any type.
You can set it with
`global_menu_set_item_tag<class_DisplayServer_method_global_menu_set_item_tag>`,
which provides a simple way of assigning context data to items.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **global\_menu\_get\_item\_text**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_text>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the text of the item at index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **global\_menu\_get\_item\_tooltip**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_item_tooltip>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns the tooltip associated with the specified index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**global\_menu\_get\_system\_menu\_roots**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_get_system_menu_roots>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns Dictionary of supported system menu IDs and names.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **global\_menu\_is\_item\_checkable**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_is_item_checkable>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns `true` if the item at index `idx` is checkable in some way, i.e.
if it has a checkbox or radio button.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **global\_menu\_is\_item\_checked**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_is_item_checked>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns `true` if the item at index `idx` is checked.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **global\_menu\_is\_item\_disabled**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_is_item_disabled>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns `true` if the item at index `idx` is disabled. When it is
disabled it can't be selected, or its action invoked.

See
`global_menu_set_item_disabled<class_DisplayServer_method_global_menu_set_item_disabled>`
for more info on how to disable an item.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **global\_menu\_is\_item\_hidden**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_is_item_hidden>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns `true` if the item at index `idx` is hidden.

See
`global_menu_set_item_hidden<class_DisplayServer_method_global_menu_set_item_hidden>`
for more info on how to hide an item.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**global\_menu\_is\_item\_radio\_checkable**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_global_menu_is_item_radio_checkable>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Returns `true` if the item at index `idx` has radio button-style
checkability.

\*\*Note:\*\* This is purely cosmetic; you must add the logic for
checking/unchecking items in radio groups.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_menu\_remove\_item**(menu\_root:
`String<class_String>`, idx: `int<class_int>`)
`🔗<class_DisplayServer_method_global_menu_remove_item>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Removes the item at index `idx` from the global menu `menu_root`.

\*\*Note:\*\* The indices of items after the removed item will be
shifted by one.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_accelerator**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, keycode:
`Key<enum_@GlobalScope_Key>`)
`🔗<class_DisplayServer_method_global_menu_set_item_accelerator>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the accelerator of the item at index `idx`. `keycode` can be a
single `Key<enum_@GlobalScope_Key>`, or a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_callback**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_global_menu_set_item_callback>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the callback of the item at index `idx`. Callback is emitted when
an item is pressed.

\*\*Note:\*\* The `callback` Callable needs to accept exactly one
Variant parameter, the parameter passed to the Callable will be the
value passed to the `tag` parameter when the menu item was created.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_checkable**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, checkable:
`bool<class_bool>`)
`🔗<class_DisplayServer_method_global_menu_set_item_checkable>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets whether the item at index `idx` has a checkbox. If `false`, sets
the type of the item to plain text.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_checked**(menu\_root: `String<class_String>`,
idx: `int<class_int>`, checked: `bool<class_bool>`)
`🔗<class_DisplayServer_method_global_menu_set_item_checked>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the checkstate status of the item at index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_disabled**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`🔗<class_DisplayServer_method_global_menu_set_item_disabled>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Enables/disables the item at index `idx`. When it is disabled, it can't
be selected and its action can't be invoked.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_hidden**(menu\_root: `String<class_String>`,
idx: `int<class_int>`, hidden: `bool<class_bool>`)
`🔗<class_DisplayServer_method_global_menu_set_item_hidden>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Hides/shows the item at index `idx`. When it is hidden, an item does not
appear in a menu and its action cannot be invoked.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_hover\_callbacks**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_global_menu_set_item_hover_callbacks>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the callback of the item at index `idx`. The callback is emitted
when an item is hovered.

\*\*Note:\*\* The `callback` Callable needs to accept exactly one
Variant parameter, the parameter passed to the Callable will be the
value passed to the `tag` parameter when the menu item was created.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_menu\_set\_item\_icon**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, icon:
`Texture2D<class_Texture2D>`)
`🔗<class_DisplayServer_method_global_menu_set_item_icon>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Replaces the `Texture2D<class_Texture2D>` icon of the specified `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

\*\*Note:\*\* This method is not supported by macOS "\_dock" menu items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_indentation\_level**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, level: `int<class_int>`)
`🔗<class_DisplayServer_method_global_menu_set_item_indentation_level>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the horizontal offset of the item at the given `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_key\_callback**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, key\_callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_global_menu_set_item_key_callback>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the callback of the item at index `idx`. Callback is emitted when
its accelerator is activated.

\*\*Note:\*\* The `key_callback` Callable needs to accept exactly one
Variant parameter, the parameter passed to the Callable will be the
value passed to the `tag` parameter when the menu item was created.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_max\_states**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, max\_states:
`int<class_int>`)
`🔗<class_DisplayServer_method_global_menu_set_item_max_states>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets number of state of a multistate item. See
`global_menu_add_multistate_item<class_DisplayServer_method_global_menu_add_multistate_item>`
for details.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_radio\_checkable**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, checkable:
`bool<class_bool>`)
`🔗<class_DisplayServer_method_global_menu_set_item_radio_checkable>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the type of the item at the specified index `idx` to radio button.
If `false`, sets the type of the item to plain text.

\*\*Note:\*\* This is purely cosmetic; you must add the logic for
checking/unchecking items in radio groups.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_menu\_set\_item\_state**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, state: `int<class_int>`)
`🔗<class_DisplayServer_method_global_menu_set_item_state>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the state of a multistate item. See
`global_menu_add_multistate_item<class_DisplayServer_method_global_menu_add_multistate_item>`
for details.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_submenu**(menu\_root: `String<class_String>`,
idx: `int<class_int>`, submenu: `String<class_String>`)
`🔗<class_DisplayServer_method_global_menu_set_item_submenu>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the submenu of the item at index `idx`. The submenu is the ID of a
global menu root that would be shown when the item is clicked.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_menu\_set\_item\_tag**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, tag:
`Variant<class_Variant>`)
`🔗<class_DisplayServer_method_global_menu_set_item_tag>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the metadata of an item, which may be of any type. You can later
get it with
`global_menu_get_item_tag<class_DisplayServer_method_global_menu_get_item_tag>`,
which provides a simple way of assigning context data to items.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_menu\_set\_item\_text**(menu\_root:
`String<class_String>`, idx: `int<class_int>`, text:
`String<class_String>`)
`🔗<class_DisplayServer_method_global_menu_set_item_text>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the text of the item at index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_item\_tooltip**(menu\_root: `String<class_String>`,
idx: `int<class_int>`, tooltip: `String<class_String>`)
`🔗<class_DisplayServer_method_global_menu_set_item_tooltip>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Sets the `String<class_String>` tooltip of the item at the specified
index `idx`.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**global\_menu\_set\_popup\_callbacks**(menu\_root:
`String<class_String>`, open\_callback: `Callable<class_Callable>`,
close\_callback: `Callable<class_Callable>`)
`🔗<class_DisplayServer_method_global_menu_set_popup_callbacks>`

**Deprecated:** Use `NativeMenu<class_NativeMenu>` or
`PopupMenu<class_PopupMenu>` instead.

Registers callables to emit when the menu is respectively about to show
or closed. Callback methods should have zero arguments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_additional\_outputs**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_has_additional_outputs>`

Returns `true` if any additional outputs have been registered via
`register_additional_output<class_DisplayServer_method_register_additional_output>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_feature**(feature:
`Feature<enum_DisplayServer_Feature>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_has_feature>`

Returns `true` if the specified `feature` is supported by the current
**DisplayServer**, `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_hardware\_keyboard**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_has_hardware_keyboard>`

Returns `true` if hardware keyboard is connected.

\*\*Note:\*\* This method is implemented on Android and iOS, on other
platforms this method always returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**help\_set\_search\_callbacks**(search\_callback:
`Callable<class_Callable>`, action\_callback:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_help_set_search_callbacks>`

Sets native help system search callbacks.

`search_callback` has the following arguments:
`String search_string, int result_limit` and return a
`Dictionary<class_Dictionary>` with "key, display name" pairs for the
search results. Called when the user enters search terms in the `Help`
menu.

`action_callback` has the following arguments: `String key`. Called when
the user selects a search result in the `Help` menu.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **ime\_get\_selection**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_ime_get_selection>`

Returns the text selection in the [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) composition string,
with the `Vector2i<class_Vector2i>`'s `x` component being the caret
position and `y` being the length of the selection.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **ime\_get\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_ime_get_text>`

Returns the composition string contained within the [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) window.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_dark\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_is_dark_mode>`

Returns `true` if OS is using dark mode.

\*\*Note:\*\* This method is implemented on Android, iOS, macOS,
Windows, and Linux (X11/Wayland).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_dark\_mode\_supported**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_is_dark_mode_supported>`

Returns `true` if OS supports dark mode.

\*\*Note:\*\* This method is implemented on Android, iOS, macOS,
Windows, and Linux (X11/Wayland).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_touchscreen\_available**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_is_touchscreen_available>`

Returns `true` if touch events are available (Android or iOS), the
capability is detected on the Web platform or if
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_window\_transparency\_available**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_is_window_transparency_available>`

Returns `true` if the window background can be made transparent. This
method returns `false` if
`ProjectSettings.display/window/per_pixel_transparency/allowed<class_ProjectSettings_property_display/window/per_pixel_transparency/allowed>`
is set to `false`, or if transparency is not supported by the renderer
or OS compositor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **keyboard\_get\_current\_layout**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_keyboard_get_current_layout>`

Returns active keyboard layout index.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS,
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>`
**keyboard\_get\_keycode\_from\_physical**(keycode:
`Key<enum_@GlobalScope_Key>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_keyboard_get_keycode_from_physical>`

Converts a physical (US QWERTY) `keycode` to one in the active keyboard
layout.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>`
**keyboard\_get\_label\_from\_physical**(keycode:
`Key<enum_@GlobalScope_Key>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_keyboard_get_label_from_physical>`

Converts a physical (US QWERTY) `keycode` to localized label printed on
the key in the active keyboard layout.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **keyboard\_get\_layout\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_keyboard_get_layout_count>`

Returns the number of keyboard layouts.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **keyboard\_get\_layout\_language**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_keyboard_get_layout_language>`

Returns the ISO-639/BCP-47 language code of the keyboard layout at
position `index`.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **keyboard\_get\_layout\_name**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_keyboard_get_layout_name>`

Returns the localized name of the keyboard layout at position `index`.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **keyboard\_set\_current\_layout**(index:
`int<class_int>`)
`🔗<class_DisplayServer_method_keyboard_set_current_layout>`

Sets the active keyboard layout.

\*\*Note:\*\* This method is implemented on Linux (X11/Wayland), macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`MouseButtonMask<enum_@GlobalScope_MouseButtonMask>`\]
**mouse\_get\_button\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_mouse_get_button_state>`

Returns the current state of mouse buttons (whether each button is
pressed) as a bitmask. If multiple mouse buttons are pressed at the same
time, the bits are added together. Equivalent to
`Input.get_mouse_button_mask<class_Input_method_get_mouse_button_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`MouseMode<enum_DisplayServer_MouseMode>` **mouse\_get\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_mouse_get_mode>`

Returns the current mouse mode. See also
`mouse_set_mode<class_DisplayServer_method_mouse_set_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **mouse\_get\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_mouse_get_position>`

Returns the mouse cursor's current position in screen coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mouse\_set\_mode**(mouse\_mode:
`MouseMode<enum_DisplayServer_MouseMode>`)
`🔗<class_DisplayServer_method_mouse_set_mode>`

Sets the current mouse mode. See also
`mouse_get_mode<class_DisplayServer_method_mouse_get_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **process\_events**()
`🔗<class_DisplayServer_method_process_events>`

Perform window manager processing, including input flushing. See also
`force_process_and_drop_events<class_DisplayServer_method_force_process_and_drop_events>`,
`Input.flush_buffered_events<class_Input_method_flush_buffered_events>`
and
`Input.use_accumulated_input<class_Input_property_use_accumulated_input>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **register\_additional\_output**(object:
`Object<class_Object>`)
`🔗<class_DisplayServer_method_register_additional_output>`

Registers an `Object<class_Object>` which represents an additional
output that will be rendered too, beyond normal windows. The
`Object<class_Object>` is only used as an identifier, which can be later
passed to
`unregister_additional_output<class_DisplayServer_method_unregister_additional_output>`.

This can be used to prevent Godot from skipping rendering when no normal
windows are visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **screen\_get\_dpi**(screen: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_dpi>`

Returns the dots per inch density of the specified screen. If `screen`
is
`SCREEN_OF_MAIN_WINDOW<class_DisplayServer_constant_SCREEN_OF_MAIN_WINDOW>`
(the default value), a screen with the main window will be used.

\*\*Note:\*\* On macOS, returned value is inaccurate if fractional
display scaling mode is used.

\*\*Note:\*\* On Android devices, the actual screen densities are
grouped into six generalized densities:

    ldpi - 120 dpi
    mdpi - 160 dpi
    hdpi - 240 dpi
    xhdpi - 320 dpi
    xxhdpi - 480 dpi
    xxxhdpi - 640 dpi

\*\*Note:\*\* This method is implemented on Android, Linux
(X11/Wayland), macOS and Windows. Returns `72` on unsupported platforms.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **screen\_get\_image**(screen: `int<class_int>` =
-1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_image>`

Returns screenshot of the `screen`.

\*\*Note:\*\* This method is implemented on Linux (X11), macOS, and
Windows.

\*\*Note:\*\* On macOS, this method requires "Screen Recording"
permission, if permission is not granted it will return desktop
wallpaper color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **screen\_get\_max\_scale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_max_scale>`

Returns the greatest scale factor of all screens.

\*\*Note:\*\* On macOS returned value is `2.0` if there is at least one
hiDPI (Retina) screen in the system, and `1.0` in all other cases.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`
**screen\_get\_orientation**(screen: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_orientation>`

Returns the `screen`'s current orientation. See also
`screen_set_orientation<class_DisplayServer_method_screen_set_orientation>`.

\*\*Note:\*\* This method is implemented on Android and iOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **screen\_get\_pixel**(position:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_pixel>`

Returns color of the display pixel at the `position`.

\*\*Note:\*\* This method is implemented on Linux (X11), macOS, and
Windows.

\*\*Note:\*\* On macOS, this method requires "Screen Recording"
permission, if permission is not granted it will return desktop
wallpaper color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **screen\_get\_position**(screen:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_position>`

Returns the screen's top-left corner position in pixels. On
multi-monitor setups, the screen position is relative to the virtual
desktop area. On multi-monitor setups with different screen resolutions
or orientations, the origin may be located outside any display like
this:

    * (0, 0)        +-------+
                    |       |
    +-------------+ |       |
    |             | |       |
    |             | |       |
    +-------------+ +-------+

See also `screen_get_size<class_DisplayServer_method_screen_get_size>`.

\*\*Note:\*\* On Linux (Wayland) this method always returns `(0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **screen\_get\_refresh\_rate**(screen:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_refresh_rate>`

Returns the current refresh rate of the specified screen. If `screen` is
`SCREEN_OF_MAIN_WINDOW<class_DisplayServer_constant_SCREEN_OF_MAIN_WINDOW>`
(the default value), a screen with the main window will be used.

\*\*Note:\*\* Returns `-1.0` if the DisplayServer fails to find the
refresh rate for the specified screen. On Web,
`screen_get_refresh_rate<class_DisplayServer_method_screen_get_refresh_rate>`
will always return `-1.0` as there is no way to retrieve the refresh
rate on that platform.

To fallback to a default refresh rate if the method fails, try:

    var refresh_rate = DisplayServer.screen_get_refresh_rate()
    if refresh_rate < 0:
        refresh_rate = 60.0

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **screen\_get\_scale**(screen: `int<class_int>` =
-1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_scale>`

Returns the scale factor of the specified screen by index.

\*\*Note:\*\* On macOS, the returned value is `2.0` for hiDPI (Retina)
screens, and `1.0` for all other cases.

\*\*Note:\*\* On Linux (Wayland), the returned value is accurate only
when `screen` is
`SCREEN_OF_MAIN_WINDOW<class_DisplayServer_constant_SCREEN_OF_MAIN_WINDOW>`.
Due to API limitations, passing a direct index will return a rounded-up
integer, if the screen has a fractional scale (e.g. `1.25` would get
rounded up to `2.0`).

\*\*Note:\*\* This method is implemented only on macOS and Linux
(Wayland).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **screen\_get\_size**(screen:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_size>`

Returns the screen's size in pixels. See also
`screen_get_position<class_DisplayServer_method_screen_get_position>`
and
`screen_get_usable_rect<class_DisplayServer_method_screen_get_usable_rect>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **screen\_get\_usable\_rect**(screen:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_get_usable_rect>`

Returns the portion of the screen that is not obstructed by a status bar
in pixels. See also
`screen_get_size<class_DisplayServer_method_screen_get_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **screen\_is\_kept\_on**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_screen_is_kept_on>`

Returns `true` if the screen should never be turned off by the operating
system's power-saving measures. See also
`screen_set_keep_on<class_DisplayServer_method_screen_set_keep_on>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **screen\_set\_keep\_on**(enable:
`bool<class_bool>`) `🔗<class_DisplayServer_method_screen_set_keep_on>`

Sets whether the screen should never be turned off by the operating
system's power-saving measures. See also
`screen_is_kept_on<class_DisplayServer_method_screen_is_kept_on>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **screen\_set\_orientation**(orientation:
`ScreenOrientation<enum_DisplayServer_ScreenOrientation>`, screen:
`int<class_int>` = -1)
`🔗<class_DisplayServer_method_screen_set_orientation>`

Sets the `screen`'s `orientation`. See also
`screen_get_orientation<class_DisplayServer_method_screen_get_orientation>`.

\*\*Note:\*\* On iOS, this method has no effect if
`ProjectSettings.display/window/handheld/orientation<class_ProjectSettings_property_display/window/handheld/orientation>`
is not set to
`SCREEN_SENSOR<class_DisplayServer_constant_SCREEN_SENSOR>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_icon**(image: `Image<class_Image>`)
`🔗<class_DisplayServer_method_set_icon>`

Sets the window icon (usually displayed in the top-left corner) with an
`Image<class_Image>`. To use icons in the operating system's native
format, use
`set_native_icon<class_DisplayServer_method_set_native_icon>` instead.

\*\*Note:\*\* Requires support for
`FEATURE_ICON<class_DisplayServer_constant_FEATURE_ICON>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_native\_icon**(filename:
`String<class_String>`) `🔗<class_DisplayServer_method_set_native_icon>`

Sets the window icon (usually displayed in the top-left corner) in the
operating system's *native* format. The file at `filename` must be in
`.ico` format on Windows or `.icns` on macOS. By using specially crafted
`.ico` or `.icns` icons,
`set_native_icon<class_DisplayServer_method_set_native_icon>` allows
specifying different icons depending on the size the icon is displayed
at. This size is determined by the operating system and user preferences
(including the display scale factor). To use icons in other formats, use
`set_icon<class_DisplayServer_method_set_icon>` instead.

\*\*Note:\*\* Requires support for
`FEATURE_NATIVE_ICON<class_DisplayServer_constant_FEATURE_NATIVE_ICON>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_system\_theme\_change\_callback**(callable:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_set_system_theme_change_callback>`

Sets the `callable` that should be called when system theme settings are
changed. Callback method should have zero arguments.

\*\*Note:\*\* This method is implemented on Android, iOS, macOS,
Windows, and Linux (X11/Wayland).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **status\_indicator\_get\_rect**(id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_status_indicator_get_rect>`

Returns the rectangle for the given status indicator `id` in screen
coordinates. If the status indicator is not visible, returns an empty
`Rect2<class_Rect2>`.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **status\_indicator\_set\_callback**(id:
`int<class_int>`, callback: `Callable<class_Callable>`)
`🔗<class_DisplayServer_method_status_indicator_set_callback>`

Sets the application status indicator activation callback. `callback`
should take two arguments: `int<class_int>` mouse button index (one of
`MouseButton<enum_@GlobalScope_MouseButton>` values) and
`Vector2i<class_Vector2i>` click position in screen coordinates.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **status\_indicator\_set\_icon**(id:
`int<class_int>`, icon: `Texture2D<class_Texture2D>`)
`🔗<class_DisplayServer_method_status_indicator_set_icon>`

Sets the application status indicator icon.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **status\_indicator\_set\_menu**(id:
`int<class_int>`, menu\_rid: `RID<class_RID>`)
`🔗<class_DisplayServer_method_status_indicator_set_menu>`

Sets the application status indicator native popup menu.

\*\*Note:\*\* On macOS, the menu is activated by any mouse button. Its
activation callback is *not* triggered.

\*\*Note:\*\* On Windows, the menu is activated by the right mouse
button, selecting the status icon and pressing `Shift + F10`, or the
applications key. The menu's activation callback for the other mouse
buttons is still triggered.

\*\*Note:\*\* Native popup is only supported if
`NativeMenu<class_NativeMenu>` supports the
`NativeMenu.FEATURE_POPUP_MENU<class_NativeMenu_constant_FEATURE_POPUP_MENU>`
feature.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **status\_indicator\_set\_tooltip**(id:
`int<class_int>`, tooltip: `String<class_String>`)
`🔗<class_DisplayServer_method_status_indicator_set_tooltip>`

Sets the application status indicator tooltip.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **tablet\_get\_current\_driver**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tablet_get_current_driver>`

Returns current active tablet driver name.

\*\*Note:\*\* This method is implemented only on Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **tablet\_get\_driver\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tablet_get_driver_count>`

Returns the total number of available tablet drivers.

\*\*Note:\*\* This method is implemented only on Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **tablet\_get\_driver\_name**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tablet_get_driver_name>`

Returns the tablet driver name for the given index.

\*\*Note:\*\* This method is implemented only on Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tablet\_set\_current\_driver**(name:
`String<class_String>`)
`🔗<class_DisplayServer_method_tablet_set_current_driver>`

Set active tablet driver name.

Supported drivers:

-   `winink`: Windows Ink API, default (Windows 8.1+ required).
-   `wintab`: Wacom Wintab API (compatible device driver required).
-   `dummy`: Dummy driver, tablet input is disabled.

\*\*Note:\*\* This method is implemented only on Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**tts\_get\_voices**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tts_get_voices>`

Returns an `Array<class_Array>` of voice information dictionaries.

Each `Dictionary<class_Dictionary>` contains two `String<class_String>`
entries:

-   `name` is voice name.
-   `id` is voice identifier.
-   `language` is language code in `lang_Variant` format. The `lang`
    part is a 2 or 3-letter code based on the ISO-639 standard, in
    lowercase. The `Variant` part is an engine-dependent string
    describing country, region or/and dialect.

Note that Godot depends on system libraries for text-to-speech
functionality. These libraries are installed by default on Windows and
macOS, but not on all Linux distributions. If they are not present, this
method will return an empty list. This applies to both Godot users on
Linux, as well as end-users on Linux running Godot games that use
text-to-speech.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**tts\_get\_voices\_for\_language**(language: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tts_get_voices_for_language>`

Returns an `PackedStringArray<class_PackedStringArray>` of voice
identifiers for the `language`.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **tts\_is\_paused**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tts_is_paused>`

Returns `true` if the synthesizer is in a paused state.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **tts\_is\_speaking**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_tts_is_speaking>`

Returns `true` if the synthesizer is generating speech, or have
utterance waiting in the queue.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tts\_pause**()
`🔗<class_DisplayServer_method_tts_pause>`

Puts the synthesizer into a paused state.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tts\_resume**()
`🔗<class_DisplayServer_method_tts_resume>`

Resumes the synthesizer if it was paused.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tts\_set\_utterance\_callback**(event:
`TTSUtteranceEvent<enum_DisplayServer_TTSUtteranceEvent>`, callable:
`Callable<class_Callable>`)
`🔗<class_DisplayServer_method_tts_set_utterance_callback>`

Adds a callback, which is called when the utterance has started,
finished, canceled or reached a text boundary.

-   `TTS_UTTERANCE_STARTED<class_DisplayServer_constant_TTS_UTTERANCE_STARTED>`,
    `TTS_UTTERANCE_ENDED<class_DisplayServer_constant_TTS_UTTERANCE_ENDED>`,
    and
    `TTS_UTTERANCE_CANCELED<class_DisplayServer_constant_TTS_UTTERANCE_CANCELED>`
    callable's method should take one `int<class_int>` parameter, the
    utterance ID.
-   `TTS_UTTERANCE_BOUNDARY<class_DisplayServer_constant_TTS_UTTERANCE_BOUNDARY>`
    callable's method should take two `int<class_int>` parameters, the
    index of the character and the utterance ID.

\*\*Note:\*\* The granularity of the boundary callbacks is engine
dependent.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tts\_speak**(text: `String<class_String>`,
voice: `String<class_String>`, volume: `int<class_int>` = 50, pitch:
`float<class_float>` = 1.0, rate: `float<class_float>` = 1.0,
utterance\_id: `int<class_int>` = 0, interrupt: `bool<class_bool>` =
false) `🔗<class_DisplayServer_method_tts_speak>`

Adds an utterance to the queue. If `interrupt` is `true`, the queue is
cleared first.

-   `voice` identifier is one of the `"id"` values returned by
    `tts_get_voices<class_DisplayServer_method_tts_get_voices>` or one
    of the values returned by
    `tts_get_voices_for_language<class_DisplayServer_method_tts_get_voices_for_language>`.
-   `volume` ranges from `0` (lowest) to `100` (highest).
-   `pitch` ranges from `0.0` (lowest) to `2.0` (highest), `1.0` is
    default pitch for the current voice.
-   `rate` ranges from `0.1` (lowest) to `10.0` (highest), `1.0` is a
    normal speaking rate. Other values act as a percentage relative.
-   `utterance_id` is passed as a parameter to the callback functions.

\*\*Note:\*\* On Windows and Linux (X11/Wayland), utterance `text` can
use SSML markup. SSML support is engine and voice dependent. If the
engine does not support SSML, you should strip out all XML markup before
calling `tts_speak<class_DisplayServer_method_tts_speak>`.

\*\*Note:\*\* The granularity of pitch, rate, and volume is engine and
voice dependent. Values may be truncated.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Wayland), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tts\_stop**()
`🔗<class_DisplayServer_method_tts_stop>`

Stops synthesis in progress and removes all utterances from the queue.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux
(X11/Linux), macOS, and Windows.

\*\*Note:\*\*
`ProjectSettings.audio/general/text_to_speech<class_ProjectSettings_property_audio/general/text_to_speech>`
should be `true` to use text-to-speech.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unregister\_additional\_output**(object:
`Object<class_Object>`)
`🔗<class_DisplayServer_method_unregister_additional_output>`

Unregisters an `Object<class_Object>` representing an additional output,
that was registered via
`register_additional_output<class_DisplayServer_method_register_additional_output>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **virtual\_keyboard\_get\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_virtual_keyboard_get_height>`

Returns the on-screen keyboard's height in pixels. Returns 0 if there is
no keyboard or if it is currently hidden.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **virtual\_keyboard\_hide**()
`🔗<class_DisplayServer_method_virtual_keyboard_hide>`

Hides the virtual keyboard if it is shown, does nothing otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **virtual\_keyboard\_show**(existing\_text:
`String<class_String>`, position: `Rect2<class_Rect2>` = Rect2(0, 0, 0,
0), type: `VirtualKeyboardType<enum_DisplayServer_VirtualKeyboardType>`
= 0, max\_length: `int<class_int>` = -1, cursor\_start: `int<class_int>`
= -1, cursor\_end: `int<class_int>` = -1)
`🔗<class_DisplayServer_method_virtual_keyboard_show>`

Shows the virtual keyboard if the platform has one.

`existing_text` parameter is useful for implementing your own
`LineEdit<class_LineEdit>` or `TextEdit<class_TextEdit>`, as it tells
the virtual keyboard what text has already been typed (the virtual
keyboard uses it for auto-correct and predictions).

`position` parameter is the screen space `Rect2<class_Rect2>` of the
edited text.

`type` parameter allows configuring which type of virtual keyboard to
show.

`max_length` limits the number of characters that can be entered if
different from `-1`.

`cursor_start` can optionally define the current text cursor position if
`cursor_end` is not set.

`cursor_start` and `cursor_end` can optionally define the current text
selection.

\*\*Note:\*\* This method is implemented on Android, iOS and Web.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **warp\_mouse**(position:
`Vector2i<class_Vector2i>`) `🔗<class_DisplayServer_method_warp_mouse>`

Sets the mouse cursor position to the given `position` relative to an
origin at the upper left corner of the currently focused game Window
Manager window.

\*\*Note:\*\* `warp_mouse<class_DisplayServer_method_warp_mouse>` is
only supported on Windows, macOS, and Linux (X11/Wayland). It has no
effect on Android, iOS, and Web.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **window\_can\_draw**(window\_id: `int<class_int>` =
0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_can_draw>`

Returns `true` if anything can be drawn in the window specified by
`window_id`, `false` otherwise. Using the `--disable-render-loop`
command line argument or a headless build will return `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **window\_get\_active\_popup**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_active_popup>`

Returns ID of the active popup window, or
`INVALID_WINDOW_ID<class_DisplayServer_constant_INVALID_WINDOW_ID>` if
there is none.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **window\_get\_attached\_instance\_id**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_attached_instance_id>`

Returns the
`Object.get_instance_id<class_Object_method_get_instance_id>` of the
`Window<class_Window>` the `window_id` is attached to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **window\_get\_current\_screen**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_current_screen>`

Returns the screen the window specified by `window_id` is currently
positioned on. If the screen overlaps multiple displays, the screen
where the window's center is located is returned. See also
`window_set_current_screen<class_DisplayServer_method_window_set_current_screen>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **window\_get\_flag**(flag:
`WindowFlags<enum_DisplayServer_WindowFlags>`, window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_flag>`

Returns the current value of the given window's `flag`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **window\_get\_max\_size**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_max_size>`

Returns the window's maximum size (in pixels). See also
`window_set_max_size<class_DisplayServer_method_window_set_max_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **window\_get\_min\_size**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_min_size>`

Returns the window's minimum size (in pixels). See also
`window_set_min_size<class_DisplayServer_method_window_set_min_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`WindowMode<enum_DisplayServer_WindowMode>`
**window\_get\_mode**(window\_id: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_mode>`

Returns the mode of the given window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **window\_get\_native\_handle**(handle\_type:
`HandleType<enum_DisplayServer_HandleType>`, window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_native_handle>`

Returns internal structure pointers for use in plugins.

\*\*Note:\*\* This method is implemented on Android, Linux
(X11/Wayland), macOS, and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **window\_get\_popup\_safe\_rect**(window:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_popup_safe_rect>`

Returns the bounding box of control, or menu item that was used to open
the popup window, in the screen coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **window\_get\_position**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_position>`

Returns the position of the client area of the given window on the
screen.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>`
**window\_get\_position\_with\_decorations**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_position_with_decorations>`

Returns the position of the given window on the screen including the
borders drawn by the operating system. See also
`window_get_position<class_DisplayServer_method_window_get_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3i<class_Vector3i>`
**window\_get\_safe\_title\_margins**(window\_id: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_safe_title_margins>`

Returns left margins (`x`), right margins (`y`) and height (`z`) of the
title that are safe to use (contains no buttons or other elements) when
`WINDOW_FLAG_EXTEND_TO_TITLE<class_DisplayServer_constant_WINDOW_FLAG_EXTEND_TO_TITLE>`
flag is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **window\_get\_size**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_size>`

Returns the size of the window specified by `window_id` (in pixels),
excluding the borders drawn by the operating system. This is also called
the "client area". See also
`window_get_size_with_decorations<class_DisplayServer_method_window_get_size_with_decorations>`,
`window_set_size<class_DisplayServer_method_window_set_size>` and
`window_get_position<class_DisplayServer_method_window_get_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>`
**window\_get\_size\_with\_decorations**(window\_id: `int<class_int>` =
0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_size_with_decorations>`

Returns the size of the window specified by `window_id` (in pixels),
including the borders drawn by the operating system. See also
`window_get_size<class_DisplayServer_method_window_get_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **window\_get\_title\_size**(title:
`String<class_String>`, window\_id: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_title_size>`

Returns the estimated window title bar size (including text and window
buttons) for the window specified by `window_id` (in pixels). This
method does not change the window title.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VSyncMode<enum_DisplayServer_VSyncMode>`
**window\_get\_vsync\_mode**(window\_id: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_get_vsync_mode>`

Returns the V-Sync mode of the given window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **window\_is\_focused**(window\_id: `int<class_int>`
= 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_is_focused>`

Returns `true` if the window specified by `window_id` is focused.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **window\_is\_maximize\_allowed**(window\_id:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_is_maximize_allowed>`

Returns `true` if the given window can be maximized (the maximize button
is enabled).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **window\_maximize\_on\_title\_dbl\_click**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_maximize_on_title_dbl_click>`

Returns `true`, if double-click on a window title should maximize it.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **window\_minimize\_on\_title\_dbl\_click**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DisplayServer_method_window_minimize_on_title_dbl_click>`

Returns `true`, if double-click on a window title should minimize it.

\*\*Note:\*\* This method is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_move\_to\_foreground**(window\_id:
`int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_move_to_foreground>`

Moves the window specified by `window_id` to the foreground, so that it
is visible over other windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_request\_attention**(window\_id:
`int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_request_attention>`

Makes the window specified by `window_id` request attention, which is
materialized by the window title and taskbar entry blinking until the
window is focused. This usually has no visible effect if the window is
currently focused. The exact behavior varies depending on the operating
system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_current\_screen**(screen:
`int<class_int>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_current_screen>`

Moves the window specified by `window_id` to the specified `screen`. See
also
`window_get_current_screen<class_DisplayServer_method_window_get_current_screen>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**window\_set\_drop\_files\_callback**(callback:
`Callable<class_Callable>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_drop_files_callback>`

Sets the `callback` that should be called when files are dropped from
the operating system's file manager to the window specified by
`window_id`. `callback` should take one
`PackedStringArray<class_PackedStringArray>` argument, which is the list
of dropped files.

\*\*Warning:\*\* Advanced users only! Adding such a callback to a
`Window<class_Window>` node will override its default implementation,
which can introduce bugs.

\*\*Note:\*\* This method is implemented on Windows, macOS, Linux
(X11/Wayland), and Web.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_exclusive**(window\_id:
`int<class_int>`, exclusive: `bool<class_bool>`)
`🔗<class_DisplayServer_method_window_set_exclusive>`

If set to `true`, this window will always stay on top of its parent
window, parent window will ignore input while this window is opened.

\*\*Note:\*\* On macOS, exclusive windows are confined to the same space
(virtual desktop or screen) as the parent window.

\*\*Note:\*\* This method is implemented on macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_flag**(flag:
`WindowFlags<enum_DisplayServer_WindowFlags>`, enabled:
`bool<class_bool>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_flag>`

Enables or disables the given window's given `flag`. See
`WindowFlags<enum_DisplayServer_WindowFlags>` for possible values and
their behavior.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_ime\_active**(active:
`bool<class_bool>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_ime_active>`

Sets whether [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) should be enabled
for the window specified by `window_id`. See also
`window_set_ime_position<class_DisplayServer_method_window_set_ime_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_ime\_position**(position:
`Vector2i<class_Vector2i>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_ime_position>`

Sets the position of the [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) popup for the
specified `window_id`. Only effective if
`window_set_ime_active<class_DisplayServer_method_window_set_ime_active>`
was set to `true` for the specified `window_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**window\_set\_input\_event\_callback**(callback:
`Callable<class_Callable>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_input_event_callback>`

Sets the `callback` that should be called when any
`InputEvent<class_InputEvent>` is sent to the window specified by
`window_id`.

\*\*Warning:\*\* Advanced users only! Adding such a callback to a
`Window<class_Window>` node will override its default implementation,
which can introduce bugs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**window\_set\_input\_text\_callback**(callback:
`Callable<class_Callable>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_input_text_callback>`

Sets the `callback` that should be called when text is entered using the
virtual keyboard to the window specified by `window_id`.

\*\*Warning:\*\* Advanced users only! Adding such a callback to a
`Window<class_Window>` node will override its default implementation,
which can introduce bugs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_max\_size**(max\_size:
`Vector2i<class_Vector2i>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_max_size>`

Sets the maximum size of the window specified by `window_id` in pixels.
Normally, the user will not be able to drag the window to make it larger
than the specified size. See also
`window_get_max_size<class_DisplayServer_method_window_get_max_size>`.

\*\*Note:\*\* It's recommended to change this value using
`Window.max_size<class_Window_property_max_size>` instead.

\*\*Note:\*\* Using third-party tools, it is possible for users to
disable window geometry restrictions and therefore bypass this limit.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_min\_size**(min\_size:
`Vector2i<class_Vector2i>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_min_size>`

Sets the minimum size for the given window to `min_size` in pixels.
Normally, the user will not be able to drag the window to make it
smaller than the specified size. See also
`window_get_min_size<class_DisplayServer_method_window_get_min_size>`.

\*\*Note:\*\* It's recommended to change this value using
`Window.min_size<class_Window_property_min_size>` instead.

\*\*Note:\*\* By default, the main window has a minimum size of
`Vector2i(64, 64)`. This prevents issues that can arise when the window
is resized to a near-zero size.

\*\*Note:\*\* Using third-party tools, it is possible for users to
disable window geometry restrictions and therefore bypass this limit.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_mode**(mode:
`WindowMode<enum_DisplayServer_WindowMode>`, window\_id:
`int<class_int>` = 0) `🔗<class_DisplayServer_method_window_set_mode>`

Sets window mode for the given window to `mode`. See
`WindowMode<enum_DisplayServer_WindowMode>` for possible values and how
each mode behaves.

\*\*Note:\*\* Setting the window to full screen forcibly sets the
borderless flag to `true`, so make sure to set it back to `false` when
not wanted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_mouse\_passthrough**(region:
`PackedVector2Array<class_PackedVector2Array>`, window\_id:
`int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_mouse_passthrough>`

Sets a polygonal region of the window which accepts mouse events. Mouse
events outside the region will be passed through.

Passing an empty array will disable passthrough support (all mouse
events will be intercepted by the window, which is the default
behavior).

gdscript

\# Set region, using Path2D node.
DisplayServer.window\_set\_mouse\_passthrough($Path2D.curve.get\_baked\_points())

\# Set region, using Polygon2D node.
DisplayServer.window\_set\_mouse\_passthrough($Polygon2D.polygon)

\# Reset region to default.
DisplayServer.window\_set\_mouse\_passthrough(\[\])

csharp

// Set region, using Path2D node.
DisplayServer.WindowSetMousePassthrough(GetNode&lt;Path2D&gt;("Path2D").Curve.GetBakedPoints());

// Set region, using Polygon2D node.
DisplayServer.WindowSetMousePassthrough(GetNode&lt;Polygon2D&gt;("Polygon2D").Polygon);

// Reset region to default. DisplayServer.WindowSetMousePassthrough(new
Vector2\[\] {});

\*\*Note:\*\* On Windows, the portion of a window that lies outside the
region is not drawn, while on Linux (X11) and macOS it is.

\*\*Note:\*\* This method is implemented on Linux (X11), macOS and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_popup\_safe\_rect**(window:
`int<class_int>`, rect: `Rect2i<class_Rect2i>`)
`🔗<class_DisplayServer_method_window_set_popup_safe_rect>`

Sets the bounding box of control, or menu item that was used to open the
popup window, in the screen coordinate system. Clicking this area will
not auto-close this popup.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_position**(position:
`Vector2i<class_Vector2i>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_position>`

Sets the position of the given window to `position`. On multi-monitor
setups, the screen position is relative to the virtual desktop area. On
multi-monitor setups with different screen resolutions or orientations,
the origin may be located outside any display like this:

    * (0, 0)        +-------+
                    |       |
    +-------------+ |       |
    |             | |       |
    |             | |       |
    +-------------+ +-------+

See also
`window_get_position<class_DisplayServer_method_window_get_position>`
and `window_set_size<class_DisplayServer_method_window_set_size>`.

\*\*Note:\*\* It's recommended to change this value using
`Window.position<class_Window_property_position>` instead.

\*\*Note:\*\* On Linux (Wayland): this method is a no-op.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**window\_set\_rect\_changed\_callback**(callback:
`Callable<class_Callable>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_rect_changed_callback>`

Sets the `callback` that will be called when the window specified by
`window_id` is moved or resized.

\*\*Warning:\*\* Advanced users only! Adding such a callback to a
`Window<class_Window>` node will override its default implementation,
which can introduce bugs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_size**(size:
`Vector2i<class_Vector2i>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_size>`

Sets the size of the given window to `size` (in pixels). See also
`window_get_size<class_DisplayServer_method_window_get_size>` and
`window_get_position<class_DisplayServer_method_window_get_position>`.

\*\*Note:\*\* It's recommended to change this value using
`Window.size<class_Window_property_size>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_title**(title:
`String<class_String>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_title>`

Sets the title of the given window to `title`.

\*\*Note:\*\* It's recommended to change this value using
`Window.title<class_Window_property_title>` instead.

\*\*Note:\*\* Avoid changing the window title every frame, as this can
cause performance issues on certain window managers. Try to change the
window title only a few times per second at most.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_transient**(window\_id:
`int<class_int>`, parent\_window\_id: `int<class_int>`)
`🔗<class_DisplayServer_method_window_set_transient>`

Sets window transient parent. Transient window will be destroyed with
its transient parent and will return focus to their parent when closed.
The transient window is displayed on top of a non-exclusive full-screen
parent window. Transient windows can't enter full-screen mode.

\*\*Note:\*\* It's recommended to change this value using
`Window.transient<class_Window_property_transient>` instead.

\*\*Note:\*\* The behavior might be different depending on the platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **window\_set\_vsync\_mode**(vsync\_mode:
`VSyncMode<enum_DisplayServer_VSyncMode>`, window\_id: `int<class_int>`
= 0) `🔗<class_DisplayServer_method_window_set_vsync_mode>`

Sets the V-Sync mode of the given window. See also
`ProjectSettings.display/window/vsync/vsync_mode<class_ProjectSettings_property_display/window/vsync/vsync_mode>`.

See `VSyncMode<enum_DisplayServer_VSyncMode>` for possible values and
how they affect the behavior of your application.

Depending on the platform and used renderer, the engine will fall back
to `VSYNC_ENABLED<class_DisplayServer_constant_VSYNC_ENABLED>` if the
desired mode is not supported.

\*\*Note:\*\* V-Sync modes other than
`VSYNC_ENABLED<class_DisplayServer_constant_VSYNC_ENABLED>` are only
supported in the Forward+ and Mobile rendering methods, not
Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**window\_set\_window\_buttons\_offset**(offset:
`Vector2i<class_Vector2i>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_window_buttons_offset>`

When
`WINDOW_FLAG_EXTEND_TO_TITLE<class_DisplayServer_constant_WINDOW_FLAG_EXTEND_TO_TITLE>`
flag is set, set offset to the center of the first titlebar button.

\*\*Note:\*\* This flag is implemented only on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**window\_set\_window\_event\_callback**(callback:
`Callable<class_Callable>`, window\_id: `int<class_int>` = 0)
`🔗<class_DisplayServer_method_window_set_window_event_callback>`

Sets the `callback` that will be called when an event occurs in the
window specified by `window_id`.

\*\*Warning:\*\* Advanced users only! Adding such a callback to a
`Window<class_Window>` node will override its default implementation,
which can introduce bugs.
