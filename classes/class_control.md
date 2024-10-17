github\_url  
hide

# Control

**Inherits:** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:** `BaseButton<class_BaseButton>`,
`ColorRect<class_ColorRect>`, `Container<class_Container>`,
`GraphEdit<class_GraphEdit>`, `ItemList<class_ItemList>`,
`Label<class_Label>`, `LineEdit<class_LineEdit>`,
`MenuBar<class_MenuBar>`, `NinePatchRect<class_NinePatchRect>`,
`Panel<class_Panel>`, `Range<class_Range>`,
`ReferenceRect<class_ReferenceRect>`,
`RichTextLabel<class_RichTextLabel>`, `Separator<class_Separator>`,
`TabBar<class_TabBar>`, `TextEdit<class_TextEdit>`,
`TextureRect<class_TextureRect>`, `Tree<class_Tree>`,
`VideoStreamPlayer<class_VideoStreamPlayer>`

Base class for all GUI controls. Adapts its position and size based on
its parent control.

classref-introduction-group

## Description

Base class for all UI-related nodes. **Control** features a bounding
rectangle that defines its extents, an anchor position relative to its
parent control or the current viewport, and offsets relative to the
anchor. The offsets update automatically when the node, any of its
parents, or the screen size change.

For more information on Godot's UI system, anchors, offsets, and
containers, see the related tutorials in the manual. To build flexible
UIs, you'll need a mix of UI elements that inherit from **Control** and
`Container<class_Container>` nodes.

\*\*User Interface nodes and input\*\*

Godot propagates input events via viewports. Each
`Viewport<class_Viewport>` is responsible for propagating
`InputEvent<class_InputEvent>`s to their child nodes. As the
`SceneTree.root<class_SceneTree_property_root>` is a
`Window<class_Window>`, this already happens automatically for all UI
elements in your game.

Input events are propagated through the `SceneTree<class_SceneTree>`
from the root node to all child nodes by calling
`Node._input<class_Node_private_method__input>`. For UI elements
specifically, it makes more sense to override the virtual method
`_gui_input<class_Control_private_method__gui_input>`, which filters out
unrelated input events, such as by checking z-order,
`mouse_filter<class_Control_property_mouse_filter>`, focus, or if the
event was inside of the control's bounding box.

Call `accept_event<class_Control_method_accept_event>` so no other node
receives the event. Once you accept an input, it becomes handled so
`Node._unhandled_input<class_Node_private_method__unhandled_input>` will
not process it.

Only one **Control** node can be in focus. Only the node in focus will
receive events. To get the focus, call
`grab_focus<class_Control_method_grab_focus>`. **Control** nodes lose
focus when another node grabs it, or if you hide the node in focus.

Sets `mouse_filter<class_Control_property_mouse_filter>` to
`MOUSE_FILTER_IGNORE<class_Control_constant_MOUSE_FILTER_IGNORE>` to
tell a **Control** node to ignore mouse or touch events. You'll need it
if you place an icon on top of a button.

`Theme<class_Theme>` resources change the Control's appearance. If you
change the `Theme<class_Theme>` on a **Control** node, it affects all of
its children. To override some of the theme's parameters, call one of
the `add_theme_*_override` methods, like
`add_theme_font_override<class_Control_method_add_theme_font_override>`.
You can override the theme with the Inspector.

\*\*Note:\*\* Theme items are *not* `Object<class_Object>` properties.
This means you can't access their values using
`Object.get<class_Object_method_get>` and
`Object.set<class_Object_method_set>`. Instead, use the `get_theme_*`
and `add_theme_*_override` methods provided by this class.

classref-introduction-group

## Tutorials

-   `GUI documentation index <../tutorials/ui/index>`
-   `Custom drawing in 2D <../tutorials/2d/custom_drawing_in_2d>`
-   `Control node gallery <../tutorials/ui/control_node_gallery>`
-   `Multiple resolutions <../tutorials/rendering/multiple_resolutions>`
-   [All GUI
    Demos](https://github.com/godotengine/godot-demo-projects/tree/master/gui)

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

**focus\_entered**() `🔗<class_Control_signal_focus_entered>`

Emitted when the node gains focus.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**focus\_exited**() `🔗<class_Control_signal_focus_exited>`

Emitted when the node loses focus.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**gui\_input**(event: `InputEvent<class_InputEvent>`)
`🔗<class_Control_signal_gui_input>`

Emitted when the node receives an `InputEvent<class_InputEvent>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**minimum\_size\_changed**()
`🔗<class_Control_signal_minimum_size_changed>`

Emitted when the node's minimum size changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**mouse\_entered**() `🔗<class_Control_signal_mouse_entered>`

Emitted when the mouse cursor enters the control's (or any child
control's) visible area, that is not occluded behind other Controls or
Windows, provided its
`mouse_filter<class_Control_property_mouse_filter>` lets the event reach
it and regardless if it's currently focused or not.

\*\*Note:\*\* `CanvasItem.z_index<class_CanvasItem_property_z_index>`
doesn't affect, which Control receives the signal.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**mouse\_exited**() `🔗<class_Control_signal_mouse_exited>`

Emitted when the mouse cursor leaves the control's (and all child
control's) visible area, that is not occluded behind other Controls or
Windows, provided its
`mouse_filter<class_Control_property_mouse_filter>` lets the event reach
it and regardless if it's currently focused or not.

\*\*Note:\*\* `CanvasItem.z_index<class_CanvasItem_property_z_index>`
doesn't affect, which Control receives the signal.

\*\*Note:\*\* If you want to check whether the mouse truly left the
area, ignoring any top nodes, you can use code like this:

    func _on_mouse_exited():
        if not Rect2(Vector2(), size).has_point(get_local_mouse_position()):
            # Not hovering over area.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**resized**() `🔗<class_Control_signal_resized>`

Emitted when the control changes size.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**size\_flags\_changed**() `🔗<class_Control_signal_size_flags_changed>`

Emitted when one of the size flags changes. See
`size_flags_horizontal<class_Control_property_size_flags_horizontal>`
and `size_flags_vertical<class_Control_property_size_flags_vertical>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**theme\_changed**() `🔗<class_Control_signal_theme_changed>`

Emitted when the
`NOTIFICATION_THEME_CHANGED<class_Control_constant_NOTIFICATION_THEME_CHANGED>`
notification is sent.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FocusMode**: `🔗<enum_Control_FocusMode>`

classref-enumeration-constant

`FocusMode<enum_Control_FocusMode>` **FOCUS\_NONE** = `0`

The node cannot grab focus. Use with
`focus_mode<class_Control_property_focus_mode>`.

classref-enumeration-constant

`FocusMode<enum_Control_FocusMode>` **FOCUS\_CLICK** = `1`

The node can only grab focus on mouse clicks. Use with
`focus_mode<class_Control_property_focus_mode>`.

classref-enumeration-constant

`FocusMode<enum_Control_FocusMode>` **FOCUS\_ALL** = `2`

The node can grab focus on mouse click, using the arrows and the Tab
keys on the keyboard, or using the D-pad buttons on a gamepad. Use with
`focus_mode<class_Control_property_focus_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CursorShape**: `🔗<enum_Control_CursorShape>`

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_ARROW** = `0`

Show the system's arrow mouse cursor when the user hovers the node. Use
with
`mouse_default_cursor_shape<class_Control_property_mouse_default_cursor_shape>`.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_IBEAM** = `1`

Show the system's I-beam mouse cursor when the user hovers the node. The
I-beam pointer has a shape similar to "I". It tells the user they can
highlight or insert text.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_POINTING\_HAND** = `2`

Show the system's pointing hand mouse cursor when the user hovers the
node.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_CROSS** = `3`

Show the system's cross mouse cursor when the user hovers the node.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_WAIT** = `4`

Show the system's wait mouse cursor when the user hovers the node. Often
an hourglass.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_BUSY** = `5`

Show the system's busy mouse cursor when the user hovers the node. Often
an arrow with a small hourglass.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_DRAG** = `6`

Show the system's drag mouse cursor, often a closed fist or a cross
symbol, when the user hovers the node. It tells the user they're
currently dragging an item, like a node in the Scene dock.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_CAN\_DROP** = `7`

Show the system's drop mouse cursor when the user hovers the node. It
can be an open hand. It tells the user they can drop an item they're
currently grabbing, like a node in the Scene dock.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_FORBIDDEN** = `8`

Show the system's forbidden mouse cursor when the user hovers the node.
Often a crossed circle.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_VSIZE** = `9`

Show the system's vertical resize mouse cursor when the user hovers the
node. A double-headed vertical arrow. It tells the user they can resize
the window or the panel vertically.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_HSIZE** = `10`

Show the system's horizontal resize mouse cursor when the user hovers
the node. A double-headed horizontal arrow. It tells the user they can
resize the window or the panel horizontally.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_BDIAGSIZE** = `11`

Show the system's window resize mouse cursor when the user hovers the
node. The cursor is a double-headed arrow that goes from the bottom left
to the top right. It tells the user they can resize the window or the
panel both horizontally and vertically.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_FDIAGSIZE** = `12`

Show the system's window resize mouse cursor when the user hovers the
node. The cursor is a double-headed arrow that goes from the top left to
the bottom right, the opposite of
`CURSOR_BDIAGSIZE<class_Control_constant_CURSOR_BDIAGSIZE>`. It tells
the user they can resize the window or the panel both horizontally and
vertically.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_MOVE** = `13`

Show the system's move mouse cursor when the user hovers the node. It
shows 2 double-headed arrows at a 90 degree angle. It tells the user
they can move a UI element freely.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_VSPLIT** = `14`

Show the system's vertical split mouse cursor when the user hovers the
node. On Windows, it's the same as
`CURSOR_VSIZE<class_Control_constant_CURSOR_VSIZE>`.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_HSPLIT** = `15`

Show the system's horizontal split mouse cursor when the user hovers the
node. On Windows, it's the same as
`CURSOR_HSIZE<class_Control_constant_CURSOR_HSIZE>`.

classref-enumeration-constant

`CursorShape<enum_Control_CursorShape>` **CURSOR\_HELP** = `16`

Show the system's help mouse cursor when the user hovers the node, a
question mark.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LayoutPreset**: `🔗<enum_Control_LayoutPreset>`

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_TOP\_LEFT** = `0`

Snap all 4 anchors to the top-left of the parent control's bounds. Use
with `set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_TOP\_RIGHT** = `1`

Snap all 4 anchors to the top-right of the parent control's bounds. Use
with `set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_BOTTOM\_LEFT** = `2`

Snap all 4 anchors to the bottom-left of the parent control's bounds.
Use with `set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_BOTTOM\_RIGHT** =
`3`

Snap all 4 anchors to the bottom-right of the parent control's bounds.
Use with `set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_CENTER\_LEFT** = `4`

Snap all 4 anchors to the center of the left edge of the parent
control's bounds. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_CENTER\_TOP** = `5`

Snap all 4 anchors to the center of the top edge of the parent control's
bounds. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_CENTER\_RIGHT** =
`6`

Snap all 4 anchors to the center of the right edge of the parent
control's bounds. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_CENTER\_BOTTOM** =
`7`

Snap all 4 anchors to the center of the bottom edge of the parent
control's bounds. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_CENTER** = `8`

Snap all 4 anchors to the center of the parent control's bounds. Use
with `set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_LEFT\_WIDE** = `9`

Snap all 4 anchors to the left edge of the parent control. The left
offset becomes relative to the left edge and the top offset relative to
the top left corner of the node's parent. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_TOP\_WIDE** = `10`

Snap all 4 anchors to the top edge of the parent control. The left
offset becomes relative to the top left corner, the top offset relative
to the top edge, and the right offset relative to the top right corner
of the node's parent. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_RIGHT\_WIDE** = `11`

Snap all 4 anchors to the right edge of the parent control. The right
offset becomes relative to the right edge and the top offset relative to
the top right corner of the node's parent. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_BOTTOM\_WIDE** =
`12`

Snap all 4 anchors to the bottom edge of the parent control. The left
offset becomes relative to the bottom left corner, the bottom offset
relative to the bottom edge, and the right offset relative to the bottom
right corner of the node's parent. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_VCENTER\_WIDE** =
`13`

Snap all 4 anchors to a vertical line that cuts the parent control in
half. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_HCENTER\_WIDE** =
`14`

Snap all 4 anchors to a horizontal line that cuts the parent control in
half. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`LayoutPreset<enum_Control_LayoutPreset>` **PRESET\_FULL\_RECT** = `15`

Snap all 4 anchors to the respective corners of the parent control. Set
all 4 offsets to 0 after you applied this preset and the **Control**
will fit its parent control. Use with
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LayoutPresetMode**: `🔗<enum_Control_LayoutPresetMode>`

classref-enumeration-constant

`LayoutPresetMode<enum_Control_LayoutPresetMode>`
**PRESET\_MODE\_MINSIZE** = `0`

The control will be resized to its minimum size.

classref-enumeration-constant

`LayoutPresetMode<enum_Control_LayoutPresetMode>`
**PRESET\_MODE\_KEEP\_WIDTH** = `1`

The control's width will not change.

classref-enumeration-constant

`LayoutPresetMode<enum_Control_LayoutPresetMode>`
**PRESET\_MODE\_KEEP\_HEIGHT** = `2`

The control's height will not change.

classref-enumeration-constant

`LayoutPresetMode<enum_Control_LayoutPresetMode>`
**PRESET\_MODE\_KEEP\_SIZE** = `3`

The control's size will not change.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **SizeFlags**: `🔗<enum_Control_SizeFlags>`

classref-enumeration-constant

`SizeFlags<enum_Control_SizeFlags>` **SIZE\_SHRINK\_BEGIN** = `0`

Tells the parent `Container<class_Container>` to align the node with its
start, either the top or the left edge. It is mutually exclusive with
`SIZE_FILL<class_Control_constant_SIZE_FILL>` and other shrink size
flags, but can be used with
`SIZE_EXPAND<class_Control_constant_SIZE_EXPAND>` in some containers.
Use with
`size_flags_horizontal<class_Control_property_size_flags_horizontal>`
and `size_flags_vertical<class_Control_property_size_flags_vertical>`.

\*\*Note:\*\* Setting this flag is equal to not having any size flags.

classref-enumeration-constant

`SizeFlags<enum_Control_SizeFlags>` **SIZE\_FILL** = `1`

Tells the parent `Container<class_Container>` to expand the bounds of
this node to fill all the available space without pushing any other
node. It is mutually exclusive with shrink size flags. Use with
`size_flags_horizontal<class_Control_property_size_flags_horizontal>`
and `size_flags_vertical<class_Control_property_size_flags_vertical>`.

classref-enumeration-constant

`SizeFlags<enum_Control_SizeFlags>` **SIZE\_EXPAND** = `2`

Tells the parent `Container<class_Container>` to let this node take all
the available space on the axis you flag. If multiple neighboring nodes
are set to expand, they'll share the space based on their stretch ratio.
See
`size_flags_stretch_ratio<class_Control_property_size_flags_stretch_ratio>`.
Use with
`size_flags_horizontal<class_Control_property_size_flags_horizontal>`
and `size_flags_vertical<class_Control_property_size_flags_vertical>`.

classref-enumeration-constant

`SizeFlags<enum_Control_SizeFlags>` **SIZE\_EXPAND\_FILL** = `3`

Sets the node's size flags to both fill and expand. See
`SIZE_FILL<class_Control_constant_SIZE_FILL>` and
`SIZE_EXPAND<class_Control_constant_SIZE_EXPAND>` for more information.

classref-enumeration-constant

`SizeFlags<enum_Control_SizeFlags>` **SIZE\_SHRINK\_CENTER** = `4`

Tells the parent `Container<class_Container>` to center the node in the
available space. It is mutually exclusive with
`SIZE_FILL<class_Control_constant_SIZE_FILL>` and other shrink size
flags, but can be used with
`SIZE_EXPAND<class_Control_constant_SIZE_EXPAND>` in some containers.
Use with
`size_flags_horizontal<class_Control_property_size_flags_horizontal>`
and `size_flags_vertical<class_Control_property_size_flags_vertical>`.

classref-enumeration-constant

`SizeFlags<enum_Control_SizeFlags>` **SIZE\_SHRINK\_END** = `8`

Tells the parent `Container<class_Container>` to align the node with its
end, either the bottom or the right edge. It is mutually exclusive with
`SIZE_FILL<class_Control_constant_SIZE_FILL>` and other shrink size
flags, but can be used with
`SIZE_EXPAND<class_Control_constant_SIZE_EXPAND>` in some containers.
Use with
`size_flags_horizontal<class_Control_property_size_flags_horizontal>`
and `size_flags_vertical<class_Control_property_size_flags_vertical>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MouseFilter**: `🔗<enum_Control_MouseFilter>`

classref-enumeration-constant

`MouseFilter<enum_Control_MouseFilter>` **MOUSE\_FILTER\_STOP** = `0`

The control will receive mouse movement input events and mouse button
input events if clicked on through
`_gui_input<class_Control_private_method__gui_input>`. The control will
also receive the `mouse_entered<class_Control_signal_mouse_entered>` and
`mouse_exited<class_Control_signal_mouse_exited>` signals. These events
are automatically marked as handled, and they will not propagate further
to other controls. This also results in blocking signals in other
controls.

classref-enumeration-constant

`MouseFilter<enum_Control_MouseFilter>` **MOUSE\_FILTER\_PASS** = `1`

The control will receive mouse movement input events and mouse button
input events if clicked on through
`_gui_input<class_Control_private_method__gui_input>`. The control will
also receive the `mouse_entered<class_Control_signal_mouse_entered>` and
`mouse_exited<class_Control_signal_mouse_exited>` signals.

If this control does not handle the event, the event will propagate up
to its parent control if it has one. The event is bubbled up the node
hierarchy until it reaches a non-`CanvasItem<class_CanvasItem>`, a
control with
`MOUSE_FILTER_STOP<class_Control_constant_MOUSE_FILTER_STOP>`, or a
`CanvasItem<class_CanvasItem>` with
`CanvasItem.top_level<class_CanvasItem_property_top_level>` enabled.
This will allow signals to fire in all controls it reaches. If no
control handled it, the event will be passed to
`Node._shortcut_input<class_Node_private_method__shortcut_input>` for
further processing.

classref-enumeration-constant

`MouseFilter<enum_Control_MouseFilter>` **MOUSE\_FILTER\_IGNORE** = `2`

The control will not receive any mouse movement input events nor mouse
button input events through
`_gui_input<class_Control_private_method__gui_input>`. The control will
also not receive the `mouse_entered<class_Control_signal_mouse_entered>`
nor `mouse_exited<class_Control_signal_mouse_exited>` signals. This will
not block other controls from receiving these events or firing the
signals. Ignored events will not be handled automatically. If a child
has `MOUSE_FILTER_PASS<class_Control_constant_MOUSE_FILTER_PASS>` and an
event was passed to this control, the event will further propagate up to
the control's parent.

\*\*Note:\*\* If the control has received
`mouse_entered<class_Control_signal_mouse_entered>` but not
`mouse_exited<class_Control_signal_mouse_exited>`, changing the
`mouse_filter<class_Control_property_mouse_filter>` to
`MOUSE_FILTER_IGNORE<class_Control_constant_MOUSE_FILTER_IGNORE>` will
cause `mouse_exited<class_Control_signal_mouse_exited>` to be emitted.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GrowDirection**: `🔗<enum_Control_GrowDirection>`

classref-enumeration-constant

`GrowDirection<enum_Control_GrowDirection>` **GROW\_DIRECTION\_BEGIN** =
`0`

The control will grow to the left or top to make up if its minimum size
is changed to be greater than its current size on the respective axis.

classref-enumeration-constant

`GrowDirection<enum_Control_GrowDirection>` **GROW\_DIRECTION\_END** =
`1`

The control will grow to the right or bottom to make up if its minimum
size is changed to be greater than its current size on the respective
axis.

classref-enumeration-constant

`GrowDirection<enum_Control_GrowDirection>` **GROW\_DIRECTION\_BOTH** =
`2`

The control will grow in both directions equally to make up if its
minimum size is changed to be greater than its current size.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Anchor**: `🔗<enum_Control_Anchor>`

classref-enumeration-constant

`Anchor<enum_Control_Anchor>` **ANCHOR\_BEGIN** = `0`

Snaps one of the 4 anchor's sides to the origin of the node's `Rect`, in
the top left. Use it with one of the `anchor_*` member variables, like
`anchor_left<class_Control_property_anchor_left>`. To change all 4
anchors at once, use
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-enumeration-constant

`Anchor<enum_Control_Anchor>` **ANCHOR\_END** = `1`

Snaps one of the 4 anchor's sides to the end of the node's `Rect`, in
the bottom right. Use it with one of the `anchor_*` member variables,
like `anchor_left<class_Control_property_anchor_left>`. To change all 4
anchors at once, use
`set_anchors_preset<class_Control_method_set_anchors_preset>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LayoutDirection**: `🔗<enum_Control_LayoutDirection>`

classref-enumeration-constant

`LayoutDirection<enum_Control_LayoutDirection>`
**LAYOUT\_DIRECTION\_INHERITED** = `0`

Automatic layout direction, determined from the parent control layout
direction.

classref-enumeration-constant

`LayoutDirection<enum_Control_LayoutDirection>`
**LAYOUT\_DIRECTION\_LOCALE** = `1`

Automatic layout direction, determined from the current locale.

classref-enumeration-constant

`LayoutDirection<enum_Control_LayoutDirection>`
**LAYOUT\_DIRECTION\_LTR** = `2`

Left-to-right layout direction.

classref-enumeration-constant

`LayoutDirection<enum_Control_LayoutDirection>`
**LAYOUT\_DIRECTION\_RTL** = `3`

Right-to-left layout direction.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextDirection**: `🔗<enum_Control_TextDirection>`

classref-enumeration-constant

`TextDirection<enum_Control_TextDirection>`
**TEXT\_DIRECTION\_INHERITED** = `3`

Text writing direction is the same as layout direction.

classref-enumeration-constant

`TextDirection<enum_Control_TextDirection>` **TEXT\_DIRECTION\_AUTO** =
`0`

Automatic text writing direction, determined from the current locale and
text content.

classref-enumeration-constant

`TextDirection<enum_Control_TextDirection>` **TEXT\_DIRECTION\_LTR** =
`1`

Left-to-right text writing direction.

classref-enumeration-constant

`TextDirection<enum_Control_TextDirection>` **TEXT\_DIRECTION\_RTL** =
`2`

Right-to-left text writing direction.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_RESIZED** = `40`
`🔗<class_Control_constant_NOTIFICATION_RESIZED>`

Sent when the node changes size. Use `size<class_Control_property_size>`
to get the new size.

classref-constant

**NOTIFICATION\_MOUSE\_ENTER** = `41`
`🔗<class_Control_constant_NOTIFICATION_MOUSE_ENTER>`

Sent when the mouse cursor enters the control's (or any child control's)
visible area, that is not occluded behind other Controls or Windows,
provided its `mouse_filter<class_Control_property_mouse_filter>` lets
the event reach it and regardless if it's currently focused or not.

\*\*Note:\*\* `CanvasItem.z_index<class_CanvasItem_property_z_index>`
doesn't affect which Control receives the notification.

See also
`NOTIFICATION_MOUSE_ENTER_SELF<class_Control_constant_NOTIFICATION_MOUSE_ENTER_SELF>`.

classref-constant

**NOTIFICATION\_MOUSE\_EXIT** = `42`
`🔗<class_Control_constant_NOTIFICATION_MOUSE_EXIT>`

Sent when the mouse cursor leaves the control's (and all child
control's) visible area, that is not occluded behind other Controls or
Windows, provided its
`mouse_filter<class_Control_property_mouse_filter>` lets the event reach
it and regardless if it's currently focused or not.

\*\*Note:\*\* `CanvasItem.z_index<class_CanvasItem_property_z_index>`
doesn't affect which Control receives the notification.

See also
`NOTIFICATION_MOUSE_EXIT_SELF<class_Control_constant_NOTIFICATION_MOUSE_EXIT_SELF>`.

classref-constant

**NOTIFICATION\_MOUSE\_ENTER\_SELF** = `60`
`🔗<class_Control_constant_NOTIFICATION_MOUSE_ENTER_SELF>`

**Experimental:** The reason this notification is sent may change in the
future.

Sent when the mouse cursor enters the control's visible area, that is
not occluded behind other Controls or Windows, provided its
`mouse_filter<class_Control_property_mouse_filter>` lets the event reach
it and regardless if it's currently focused or not.

\*\*Note:\*\* `CanvasItem.z_index<class_CanvasItem_property_z_index>`
doesn't affect which Control receives the notification.

See also
`NOTIFICATION_MOUSE_ENTER<class_Control_constant_NOTIFICATION_MOUSE_ENTER>`.

classref-constant

**NOTIFICATION\_MOUSE\_EXIT\_SELF** = `61`
`🔗<class_Control_constant_NOTIFICATION_MOUSE_EXIT_SELF>`

**Experimental:** The reason this notification is sent may change in the
future.

Sent when the mouse cursor leaves the control's visible area, that is
not occluded behind other Controls or Windows, provided its
`mouse_filter<class_Control_property_mouse_filter>` lets the event reach
it and regardless if it's currently focused or not.

\*\*Note:\*\* `CanvasItem.z_index<class_CanvasItem_property_z_index>`
doesn't affect which Control receives the notification.

See also
`NOTIFICATION_MOUSE_EXIT<class_Control_constant_NOTIFICATION_MOUSE_EXIT>`.

classref-constant

**NOTIFICATION\_FOCUS\_ENTER** = `43`
`🔗<class_Control_constant_NOTIFICATION_FOCUS_ENTER>`

Sent when the node grabs focus.

classref-constant

**NOTIFICATION\_FOCUS\_EXIT** = `44`
`🔗<class_Control_constant_NOTIFICATION_FOCUS_EXIT>`

Sent when the node loses focus.

classref-constant

**NOTIFICATION\_THEME\_CHANGED** = `45`
`🔗<class_Control_constant_NOTIFICATION_THEME_CHANGED>`

Sent when the node needs to refresh its theme items. This happens in one
of the following cases:

-   The `theme<class_Control_property_theme>` property is changed on
    this node or any of its ancestors.
-   The
    `theme_type_variation<class_Control_property_theme_type_variation>`
    property is changed on this node.
-   One of the node's theme property overrides is changed.
-   The node enters the scene tree.

\*\*Note:\*\* As an optimization, this notification won't be sent from
changes that occur while this node is outside of the scene tree.
Instead, all of the theme item updates can be applied at once when the
node enters the scene tree.

\*\*Note:\*\* This notification is received alongside
`Node.NOTIFICATION_ENTER_TREE<class_Node_constant_NOTIFICATION_ENTER_TREE>`,
so if you are instantiating a scene, the child nodes will not be
initialized yet. You can use it to setup theming for this node, child
nodes created from script, or if you want to access child nodes added in
the editor, make sure the node is ready using
`Node.is_node_ready<class_Node_method_is_node_ready>`.

    func _notification(what):
        if what == NOTIFICATION_THEME_CHANGED:
            if not is_node_ready():
                await ready # Wait until ready signal.
            $Label.add_theme_color_override("font_color", Color.YELLOW)

classref-constant

**NOTIFICATION\_SCROLL\_BEGIN** = `47`
`🔗<class_Control_constant_NOTIFICATION_SCROLL_BEGIN>`

Sent when this node is inside a `ScrollContainer<class_ScrollContainer>`
which has begun being scrolled when dragging the scrollable area *with a
touch event*. This notification is *not* sent when scrolling by dragging
the scrollbar, scrolling with the mouse wheel or scrolling with
keyboard/gamepad events.

\*\*Note:\*\* This signal is only emitted on Android or iOS, or on
desktop/web platforms when
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`
is enabled.

classref-constant

**NOTIFICATION\_SCROLL\_END** = `48`
`🔗<class_Control_constant_NOTIFICATION_SCROLL_END>`

Sent when this node is inside a `ScrollContainer<class_ScrollContainer>`
which has stopped being scrolled when dragging the scrollable area *with
a touch event*. This notification is *not* sent when scrolling by
dragging the scrollbar, scrolling with the mouse wheel or scrolling with
keyboard/gamepad events.

\*\*Note:\*\* This signal is only emitted on Android or iOS, or on
desktop/web platforms when
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`
is enabled.

classref-constant

**NOTIFICATION\_LAYOUT\_DIRECTION\_CHANGED** = `49`
`🔗<class_Control_constant_NOTIFICATION_LAYOUT_DIRECTION_CHANGED>`

Sent when control layout direction is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **anchor\_bottom** = `0.0`
`🔗<class_Control_property_anchor_bottom>`

classref-property-setget

-   `float<class_float>` **get\_anchor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Anchors the bottom edge of the node to the origin, the center, or the
end of its parent control. It changes how the bottom offset updates when
the node moves or changes size. You can use one of the
`Anchor<enum_Control_Anchor>` constants for convenience.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anchor\_left** = `0.0`
`🔗<class_Control_property_anchor_left>`

classref-property-setget

-   `float<class_float>` **get\_anchor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Anchors the left edge of the node to the origin, the center or the end
of its parent control. It changes how the left offset updates when the
node moves or changes size. You can use one of the
`Anchor<enum_Control_Anchor>` constants for convenience.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anchor\_right** = `0.0`
`🔗<class_Control_property_anchor_right>`

classref-property-setget

-   `float<class_float>` **get\_anchor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Anchors the right edge of the node to the origin, the center or the end
of its parent control. It changes how the right offset updates when the
node moves or changes size. You can use one of the
`Anchor<enum_Control_Anchor>` constants for convenience.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anchor\_top** = `0.0`
`🔗<class_Control_property_anchor_top>`

classref-property-setget

-   `float<class_float>` **get\_anchor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Anchors the top edge of the node to the origin, the center or the end of
its parent control. It changes how the top offset updates when the node
moves or changes size. You can use one of the
`Anchor<enum_Control_Anchor>` constants for convenience.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **auto\_translate**
`🔗<class_Control_property_auto_translate>`

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

`bool<class_bool>` **clip\_contents** = `false`
`🔗<class_Control_property_clip_contents>`

classref-property-setget

-   `void (No return value.)` **set\_clip\_contents**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_clipping\_contents**()

Enables whether rendering of `CanvasItem<class_CanvasItem>` based
children should be clipped to this control's rectangle. If `true`, parts
of a child which would be visibly outside of this control's rectangle
will not be rendered and won't receive input.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **custom\_minimum\_size** = `Vector2(0, 0)`
`🔗<class_Control_property_custom_minimum_size>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_minimum\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_custom\_minimum\_size**()

The minimum size of the node's bounding rectangle. If you set it to a
value greater than `(0, 0)`, the node's bounding rectangle will always
have at least this size. Note that **Control** nodes have their internal
minimum size returned by
`get_minimum_size<class_Control_method_get_minimum_size>`. It depends on
the control's contents, like text, textures, or style boxes. The actual
minimum size is the maximum value of this property and the internal
minimum size (see
`get_combined_minimum_size<class_Control_method_get_combined_minimum_size>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`FocusMode<enum_Control_FocusMode>` **focus\_mode** = `0`
`🔗<class_Control_property_focus_mode>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_mode**(value:
    `FocusMode<enum_Control_FocusMode>`)
-   `FocusMode<enum_Control_FocusMode>` **get\_focus\_mode**()

The focus access mode for the control (None, Click or All). Only one
Control can be focused at the same time, and it will receive keyboard,
gamepad, and mouse signals.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **focus\_neighbor\_bottom** = `NodePath("")`
`🔗<class_Control_property_focus_neighbor_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`, neighbor:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Tells Godot which node it should give focus to if the user presses the
down arrow on the keyboard or down on a gamepad by default. You can
change the key by editing the
`ProjectSettings.input/ui_down<class_ProjectSettings_property_input/ui_down>`
input action. The node must be a **Control**. If this property is not
set, Godot will give focus to the closest **Control** to the bottom of
this one.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **focus\_neighbor\_left** = `NodePath("")`
`🔗<class_Control_property_focus_neighbor_left>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`, neighbor:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Tells Godot which node it should give focus to if the user presses the
left arrow on the keyboard or left on a gamepad by default. You can
change the key by editing the
`ProjectSettings.input/ui_left<class_ProjectSettings_property_input/ui_left>`
input action. The node must be a **Control**. If this property is not
set, Godot will give focus to the closest **Control** to the left of
this one.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **focus\_neighbor\_right** = `NodePath("")`
`🔗<class_Control_property_focus_neighbor_right>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`, neighbor:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Tells Godot which node it should give focus to if the user presses the
right arrow on the keyboard or right on a gamepad by default. You can
change the key by editing the
`ProjectSettings.input/ui_right<class_ProjectSettings_property_input/ui_right>`
input action. The node must be a **Control**. If this property is not
set, Godot will give focus to the closest **Control** to the right of
this one.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **focus\_neighbor\_top** = `NodePath("")`
`🔗<class_Control_property_focus_neighbor_top>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`, neighbor:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_focus\_neighbor**(side:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Tells Godot which node it should give focus to if the user presses the
top arrow on the keyboard or top on a gamepad by default. You can change
the key by editing the
`ProjectSettings.input/ui_up<class_ProjectSettings_property_input/ui_up>`
input action. The node must be a **Control**. If this property is not
set, Godot will give focus to the closest **Control** to the top of this
one.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **focus\_next** = `NodePath("")`
`🔗<class_Control_property_focus_next>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_next**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_focus\_next**()

Tells Godot which node it should give focus to if the user presses `Tab`
on a keyboard by default. You can change the key by editing the
`ProjectSettings.input/ui_focus_next<class_ProjectSettings_property_input/ui_focus_next>`
input action.

If this property is not set, Godot will select a "best guess" based on
surrounding nodes in the scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **focus\_previous** = `NodePath("")`
`🔗<class_Control_property_focus_previous>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_previous**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_focus\_previous**()

Tells Godot which node it should give focus to if the user presses
`Shift + Tab` on a keyboard by default. You can change the key by
editing the
`ProjectSettings.input/ui_focus_prev<class_ProjectSettings_property_input/ui_focus_prev>`
input action.

If this property is not set, Godot will select a "best guess" based on
surrounding nodes in the scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **global\_position**
`🔗<class_Control_property_global_position>`

classref-property-setget

-   `Vector2<class_Vector2>` **get\_global\_position**()

The node's global position, relative to the world (usually to the
`CanvasLayer<class_CanvasLayer>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`GrowDirection<enum_Control_GrowDirection>` **grow\_horizontal** = `1`
`🔗<class_Control_property_grow_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_h\_grow\_direction**(value:
    `GrowDirection<enum_Control_GrowDirection>`)
-   `GrowDirection<enum_Control_GrowDirection>`
    **get\_h\_grow\_direction**()

Controls the direction on the horizontal axis in which the control
should grow if its horizontal minimum size is changed to be greater than
its current size, as the control always has to be at least the minimum
size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`GrowDirection<enum_Control_GrowDirection>` **grow\_vertical** = `1`
`🔗<class_Control_property_grow_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_v\_grow\_direction**(value:
    `GrowDirection<enum_Control_GrowDirection>`)
-   `GrowDirection<enum_Control_GrowDirection>`
    **get\_v\_grow\_direction**()

Controls the direction on the vertical axis in which the control should
grow if its vertical minimum size is changed to be greater than its
current size, as the control always has to be at least the minimum size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`LayoutDirection<enum_Control_LayoutDirection>` **layout\_direction** =
`0` `🔗<class_Control_property_layout_direction>`

classref-property-setget

-   `void (No return value.)` **set\_layout\_direction**(value:
    `LayoutDirection<enum_Control_LayoutDirection>`)
-   `LayoutDirection<enum_Control_LayoutDirection>`
    **get\_layout\_direction**()

Controls layout direction and text writing direction. Right-to-left
layouts are necessary for certain languages (e.g. Arabic and Hebrew).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **localize\_numeral\_system** = `true`
`🔗<class_Control_property_localize_numeral_system>`

classref-property-setget

-   `void (No return value.)` **set\_localize\_numeral\_system**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_localizing\_numeral\_system**()

If `true`, automatically converts code line numbers, list indices,
`SpinBox<class_SpinBox>` and `ProgressBar<class_ProgressBar>` values
from the Western Arabic (0..9) to the numeral systems used in current
locale.

\*\*Note:\*\* Numbers within the text are not automatically converted,
it can be done manually, using
`TextServer.format_number<class_TextServer_method_format_number>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CursorShape<enum_Control_CursorShape>`
**mouse\_default\_cursor\_shape** = `0`
`🔗<class_Control_property_mouse_default_cursor_shape>`

classref-property-setget

-   `void (No return value.)` **set\_default\_cursor\_shape**(value:
    `CursorShape<enum_Control_CursorShape>`)
-   `CursorShape<enum_Control_CursorShape>`
    **get\_default\_cursor\_shape**()

The default cursor shape for this control. Useful for Godot plugins and
applications or games that use the system's mouse cursors.

\*\*Note:\*\* On Linux, shapes may vary depending on the cursor theme of
the system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MouseFilter<enum_Control_MouseFilter>` **mouse\_filter** = `0`
`🔗<class_Control_property_mouse_filter>`

classref-property-setget

-   `void (No return value.)` **set\_mouse\_filter**(value:
    `MouseFilter<enum_Control_MouseFilter>`)
-   `MouseFilter<enum_Control_MouseFilter>` **get\_mouse\_filter**()

Controls whether the control will be able to receive mouse button input
events through `_gui_input<class_Control_private_method__gui_input>` and
how these events should be handled. Also controls whether the control
can receive the `mouse_entered<class_Control_signal_mouse_entered>`, and
`mouse_exited<class_Control_signal_mouse_exited>` signals. See the
constants to learn what each does.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **mouse\_force\_pass\_scroll\_events** = `true`
`🔗<class_Control_property_mouse_force_pass_scroll_events>`

classref-property-setget

-   `void (No return value.)`
    **set\_force\_pass\_scroll\_events**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_force\_pass\_scroll\_events**()

When enabled, scroll wheel events processed by
`_gui_input<class_Control_private_method__gui_input>` will be passed to
the parent control even if
`mouse_filter<class_Control_property_mouse_filter>` is set to
`MOUSE_FILTER_STOP<class_Control_constant_MOUSE_FILTER_STOP>`. As it
defaults to true, this allows nested scrollable containers to work out
of the box.

You should disable it on the root of your UI if you do not want scroll
events to go to the
`Node._unhandled_input<class_Node_private_method__unhandled_input>`
processing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **offset\_bottom** = `0.0`
`🔗<class_Control_property_offset_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(side:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_offset**(offset:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Distance between the node's bottom edge and its parent control, based on
`anchor_bottom<class_Control_property_anchor_bottom>`.

Offsets are often controlled by one or multiple parent
`Container<class_Container>` nodes, so you should not modify them
manually if your node is a direct child of a
`Container<class_Container>`. Offsets update automatically when you move
or resize the node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **offset\_left** = `0.0`
`🔗<class_Control_property_offset_left>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(side:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_offset**(offset:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Distance between the node's left edge and its parent control, based on
`anchor_left<class_Control_property_anchor_left>`.

Offsets are often controlled by one or multiple parent
`Container<class_Container>` nodes, so you should not modify them
manually if your node is a direct child of a
`Container<class_Container>`. Offsets update automatically when you move
or resize the node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **offset\_right** = `0.0`
`🔗<class_Control_property_offset_right>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(side:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_offset**(offset:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Distance between the node's right edge and its parent control, based on
`anchor_right<class_Control_property_anchor_right>`.

Offsets are often controlled by one or multiple parent
`Container<class_Container>` nodes, so you should not modify them
manually if your node is a direct child of a
`Container<class_Container>`. Offsets update automatically when you move
or resize the node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **offset\_top** = `0.0`
`🔗<class_Control_property_offset_top>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(side:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_offset**(offset:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Distance between the node's top edge and its parent control, based on
`anchor_top<class_Control_property_anchor_top>`.

Offsets are often controlled by one or multiple parent
`Container<class_Container>` nodes, so you should not modify them
manually if your node is a direct child of a
`Container<class_Container>`. Offsets update automatically when you move
or resize the node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **pivot\_offset** = `Vector2(0, 0)`
`🔗<class_Control_property_pivot_offset>`

classref-property-setget

-   `void (No return value.)` **set\_pivot\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_pivot\_offset**()

By default, the node's pivot is its top-left corner. When you change its
`rotation<class_Control_property_rotation>` or
`scale<class_Control_property_scale>`, it will rotate or scale around
this pivot. Set this property to `size<class_Control_property_size>` / 2
to pivot around the Control's center.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **position** = `Vector2(0, 0)`
`🔗<class_Control_property_position>`

classref-property-setget

-   `Vector2<class_Vector2>` **get\_position**()

The node's position, relative to its containing node. It corresponds to
the rectangle's top-left corner. The property is not affected by
`pivot_offset<class_Control_property_pivot_offset>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rotation** = `0.0`
`🔗<class_Control_property_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_rotation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rotation**()

The node's rotation around its pivot, in radians. See
`pivot_offset<class_Control_property_pivot_offset>` to change the
pivot's position.

\*\*Note:\*\* This property is edited in the inspector in degrees. If
you want to use degrees in a script, use
`rotation_degrees<class_Control_property_rotation_degrees>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rotation\_degrees**
`🔗<class_Control_property_rotation_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_rotation\_degrees**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rotation\_degrees**()

Helper property to access `rotation<class_Control_property_rotation>` in
degrees instead of radians.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **scale** = `Vector2(1, 1)`
`🔗<class_Control_property_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_scale**()

The node's scale, relative to its `size<class_Control_property_size>`.
Change this property to scale the node around its
`pivot_offset<class_Control_property_pivot_offset>`. The Control's
`tooltip_text<class_Control_property_tooltip_text>` will also scale
according to this value.

\*\*Note:\*\* This property is mainly intended to be used for animation
purposes. To support multiple resolutions in your project, use an
appropriate viewport stretch mode as described in the
`documentation <../tutorials/rendering/multiple_resolutions>` instead of
scaling Controls individually.

\*\*Note:\*\*
`FontFile.oversampling<class_FontFile_property_oversampling>` does *not*
take **Control** `scale<class_Control_property_scale>` into account.
This means that scaling up/down will cause bitmap fonts and rasterized
(non-MSDF) dynamic fonts to appear blurry or pixelated. To ensure text
remains crisp regardless of scale, you can enable MSDF font rendering by
enabling
`ProjectSettings.gui/theme/default_font_multichannel_signed_distance_field<class_ProjectSettings_property_gui/theme/default_font_multichannel_signed_distance_field>`
(applies to the default project font only), or enabling **Multichannel
Signed Distance Field** in the import options of a DynamicFont for
custom fonts. On system fonts,
`SystemFont.multichannel_signed_distance_field<class_SystemFont_property_multichannel_signed_distance_field>`
can be enabled in the inspector.

\*\*Note:\*\* If the Control node is a child of a
`Container<class_Container>` node, the scale will be reset to
`Vector2(1, 1)` when the scene is instantiated. To set the Control's
scale when it's instantiated, wait for one frame using
`await get_tree().process_frame` then set its
`scale<class_Control_property_scale>` property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Node<class_Node>` **shortcut\_context**
`🔗<class_Control_property_shortcut_context>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut\_context**(value:
    `Node<class_Node>`)
-   `Node<class_Node>` **get\_shortcut\_context**()

The `Node<class_Node>` which must be a parent of the focused **Control**
for the shortcut to be activated. If `null`, the shortcut can be
activated when any control is focused (a global shortcut). This allows
shortcuts to be accepted only when the user has a certain area of the
GUI focused.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **size** = `Vector2(0, 0)`
`🔗<class_Control_property_size>`

classref-property-setget

-   `Vector2<class_Vector2>` **get\_size**()

The size of the node's bounding rectangle, in the node's coordinate
system. `Container<class_Container>` nodes update this property
automatically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SizeFlags<enum_Control_SizeFlags>`\]
**size\_flags\_horizontal** = `1`
`🔗<class_Control_property_size_flags_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_h\_size\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SizeFlags<enum_Control_SizeFlags>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SizeFlags<enum_Control_SizeFlags>`\]
    **get\_h\_size\_flags**()

Tells the parent `Container<class_Container>` nodes how they should
resize and place the node on the X axis. Use a combination of the
`SizeFlags<enum_Control_SizeFlags>` constants to change the flags. See
the constants to learn what each does.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **size\_flags\_stretch\_ratio** = `1.0`
`🔗<class_Control_property_size_flags_stretch_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_stretch\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_stretch\_ratio**()

If the node and at least one of its neighbors uses the
`SIZE_EXPAND<class_Control_constant_SIZE_EXPAND>` size flag, the parent
`Container<class_Container>` will let it take more or less space
depending on this property. If this node has a stretch ratio of 2 and
its neighbor a ratio of 1, this node will take two thirds of the
available space.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SizeFlags<enum_Control_SizeFlags>`\]
**size\_flags\_vertical** = `1`
`🔗<class_Control_property_size_flags_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_v\_size\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SizeFlags<enum_Control_SizeFlags>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SizeFlags<enum_Control_SizeFlags>`\]
    **get\_v\_size\_flags**()

Tells the parent `Container<class_Container>` nodes how they should
resize and place the node on the Y axis. Use a combination of the
`SizeFlags<enum_Control_SizeFlags>` constants to change the flags. See
the constants to learn what each does.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Theme<class_Theme>` **theme** `🔗<class_Control_property_theme>`

classref-property-setget

-   `void (No return value.)` **set\_theme**(value:
    `Theme<class_Theme>`)
-   `Theme<class_Theme>` **get\_theme**()

The `Theme<class_Theme>` resource this node and all its **Control** and
`Window<class_Window>` children use. If a child node has its own
`Theme<class_Theme>` resource set, theme items are merged with child's
definitions having higher priority.

\*\*Note:\*\* `Window<class_Window>` styles will have no effect unless
the window is embedded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **theme\_type\_variation** = `&""`
`🔗<class_Control_property_theme_type_variation>`

classref-property-setget

-   `void (No return value.)` **set\_theme\_type\_variation**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_theme\_type\_variation**()

The name of a theme type variation used by this **Control** to look up
its own theme items. When empty, the class name of the node is used
(e.g. `Button` for the `Button<class_Button>` control), as well as the
class names of all parent classes (in order of inheritance).

When set, this property gives the highest priority to the type of the
specified name. This type can in turn extend another type, forming a
dependency chain. See
`Theme.set_type_variation<class_Theme_method_set_type_variation>`. If
the theme item cannot be found using this type or its base types, lookup
falls back on the class names.

\*\*Note:\*\* To look up **Control**'s own items use various
`get_theme_*` methods without specifying `theme_type`.

\*\*Note:\*\* Theme items are looked for in the tree order, from branch
to root, where each **Control** node is checked for its
`theme<class_Control_property_theme>` property. The earliest match
against any type/class name is returned. The project-level Theme and the
default Theme are checked last.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AutoTranslateMode<enum_Node_AutoTranslateMode>`
**tooltip\_auto\_translate\_mode** = `0`
`🔗<class_Control_property_tooltip_auto_translate_mode>`

classref-property-setget

-   `void (No return value.)`
    **set\_tooltip\_auto\_translate\_mode**(value:
    `AutoTranslateMode<enum_Node_AutoTranslateMode>`)
-   `AutoTranslateMode<enum_Node_AutoTranslateMode>`
    **get\_tooltip\_auto\_translate\_mode**()

Defines if tooltip text should automatically change to its translated
version depending on the current locale. Uses the same auto translate
mode as this control when set to
`Node.AUTO_TRANSLATE_MODE_INHERIT<class_Node_constant_AUTO_TRANSLATE_MODE_INHERIT>`.

\*\*Note:\*\* When the tooltip is customized using
`_make_custom_tooltip<class_Control_private_method__make_custom_tooltip>`,
this auto translate mode is applied automatically to the returned
control.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **tooltip\_text** = `""`
`🔗<class_Control_property_tooltip_text>`

classref-property-setget

-   `void (No return value.)` **set\_tooltip\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_tooltip\_text**()

The default tooltip text. The tooltip appears when the user's mouse
cursor stays idle over this control for a few moments, provided that the
`mouse_filter<class_Control_property_mouse_filter>` property is not
`MOUSE_FILTER_IGNORE<class_Control_constant_MOUSE_FILTER_IGNORE>`. The
time required for the tooltip to appear can be changed with the
`ProjectSettings.gui/timers/tooltip_delay_sec<class_ProjectSettings_property_gui/timers/tooltip_delay_sec>`
option. See also `get_tooltip<class_Control_method_get_tooltip>`.

The tooltip popup will use either a default implementation, or a custom
one that you can provide by overriding
`_make_custom_tooltip<class_Control_private_method__make_custom_tooltip>`.
The default tooltip includes a `PopupPanel<class_PopupPanel>` and
`Label<class_Label>` whose theme properties can be customized using
`Theme<class_Theme>` methods with the `"TooltipPanel"` and
`"TooltipLabel"` respectively. For example:

gdscript

var style\_box = StyleBoxFlat.new() style\_box.set\_bg\_color(Color(1,
1, 0)) style\_box.set\_border\_width\_all(2) \# We assume here that the
<span class="title-ref">theme</span> property has been assigned a custom
Theme beforehand. theme.set\_stylebox("panel", "TooltipPanel",
style\_box) theme.set\_color("font\_color", "TooltipLabel", Color(0, 1,
1))

csharp

var styleBox = new StyleBoxFlat(); styleBox.SetBgColor(new Color(1, 1,
0)); styleBox.SetBorderWidthAll(2); // We assume here that the
<span class="title-ref">Theme</span> property has been assigned a custom
Theme beforehand. Theme.SetStyleBox("panel", "TooltipPanel", styleBox);
Theme.SetColor("font\_color", "TooltipLabel", new Color(0, 1, 1));

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_can\_drop\_data**(at\_position:
`Vector2<class_Vector2>`, data: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_private_method__can_drop_data>`

Godot calls this method to test if `data` from a control's
`_get_drag_data<class_Control_private_method__get_drag_data>` can be
dropped at `at_position`. `at_position` is local to this control.

This method should only be used to test the data. Process the data in
`_drop_data<class_Control_private_method__drop_data>`.

gdscript

func \_can\_drop\_data(position, data):  
\# Check position if it is relevant to you \# Otherwise, just check data
return typeof(data) == TYPE\_DICTIONARY and data.has("expected")

csharp

public override bool \_CanDropData(Vector2 atPosition, Variant data) {
// Check position if it is relevant to you // Otherwise, just check data
return data.VariantType == Variant.Type.Dictionary &&
data.AsGodotDictionary().ContainsKey("expected"); }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_drop\_data**(at\_position:
`Vector2<class_Vector2>`, data: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Control_private_method__drop_data>`

Godot calls this method to pass you the `data` from a control's
`_get_drag_data<class_Control_private_method__get_drag_data>` result.
Godot first calls
`_can_drop_data<class_Control_private_method__can_drop_data>` to test if
`data` is allowed to drop at `at_position` where `at_position` is local
to this control.

gdscript

func \_can\_drop\_data(position, data):  
return typeof(data) == TYPE\_DICTIONARY and data.has("color")

func \_drop\_data(position, data):  
var color = data\["color"\]

csharp

public override bool \_CanDropData(Vector2 atPosition, Variant data) {
return data.VariantType == Variant.Type.Dictionary &&
dict.AsGodotDictionary().ContainsKey("color"); }

public override void \_DropData(Vector2 atPosition, Variant data) {
Color color = data.AsGodotDictionary()\["color"\].AsColor(); }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_get\_drag\_data**(at\_position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Control_private_method__get_drag_data>`

Godot calls this method to get data that can be dragged and dropped onto
controls that expect drop data. Returns `null` if there is no data to
drag. Controls that want to receive drop data should implement
`_can_drop_data<class_Control_private_method__can_drop_data>` and
`_drop_data<class_Control_private_method__drop_data>`. `at_position` is
local to this control. Drag may be forced with
`force_drag<class_Control_method_force_drag>`.

A preview that will follow the mouse that should represent the data can
be set with `set_drag_preview<class_Control_method_set_drag_preview>`. A
good time to set the preview is in this method.

gdscript

func \_get\_drag\_data(position):  
var mydata = make\_data() \# This is your custom method generating the
drag data. set\_drag\_preview(make\_preview(mydata)) \# This is your
custom method generating the preview of the drag data. return mydata

csharp

public override Variant \_GetDragData(Vector2 atPosition) { var myData =
MakeData(); // This is your custom method generating the drag data.
SetDragPreview(MakePreview(myData)); // This is your custom method
generating the preview of the drag data. return myData; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_get\_minimum\_size**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_private_method__get_minimum_size>`

Virtual method to be implemented by the user. Returns the minimum size
for this control. Alternative to
`custom_minimum_size<class_Control_property_custom_minimum_size>` for
controlling minimum size via code. The actual minimum size will be the
max value of these two (in each axis separately).

If not overridden, defaults to
`Vector2.ZERO<class_Vector2_constant_ZERO>`.

\*\*Note:\*\* This method will not be called when the script is attached
to a **Control** node that already overrides its minimum size (e.g.
`Label<class_Label>`, `Button<class_Button>`,
`PanelContainer<class_PanelContainer>` etc.). It can only be used with
most basic GUI nodes, like **Control**, `Container<class_Container>`,
`Panel<class_Panel>` etc.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_tooltip**(at\_position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_private_method__get_tooltip>`

Virtual method to be implemented by the user. Returns the tooltip text
for the position `at_position` in control's local coordinates, which
will typically appear when the cursor is resting over this control. See
`get_tooltip<class_Control_method_get_tooltip>`.

\*\*Note:\*\* If this method returns an empty `String<class_String>`, no
tooltip is displayed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_gui\_input**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Control_private_method__gui_input>`

Virtual method to be implemented by the user. Use this method to process
and accept inputs on UI elements. See
`accept_event<class_Control_method_accept_event>`.

\*\*Example usage for clicking a control:\*\*

gdscript

func \_gui\_input(event):  
if event is InputEventMouseButton:  
if event.button\_index == MOUSE\_BUTTON\_LEFT and event.pressed:  
print("I've been clicked D:")

csharp

public override void \_GuiInput(InputEvent @event) { if (@event is
InputEventMouseButton mb) { if (mb.ButtonIndex == MouseButton.Left &&
mb.Pressed) { GD.Print("I've been clicked D:"); } } }

The event won't trigger if:

\* clicking outside the control (see
`_has_point<class_Control_private_method__has_point>`);

\* control has `mouse_filter<class_Control_property_mouse_filter>` set
to `MOUSE_FILTER_IGNORE<class_Control_constant_MOUSE_FILTER_IGNORE>`;

\* control is obstructed by another **Control** on top of it, which
doesn't have `mouse_filter<class_Control_property_mouse_filter>` set to
`MOUSE_FILTER_IGNORE<class_Control_constant_MOUSE_FILTER_IGNORE>`;

\* control's parent has
`mouse_filter<class_Control_property_mouse_filter>` set to
`MOUSE_FILTER_STOP<class_Control_constant_MOUSE_FILTER_STOP>` or has
accepted the event;

\* it happens outside the parent's rectangle and the parent has either
`clip_contents<class_Control_property_clip_contents>` enabled.

\*\*Note:\*\* Event position is relative to the control origin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_point**(point: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_private_method__has_point>`

Virtual method to be implemented by the user. Returns whether the given
`point` is inside this control.

If not overridden, default behavior is checking if the point is within
control's Rect.

\*\*Note:\*\* If you want to check if a point is inside the control, you
can use `Rect2(Vector2.ZERO, size).has_point(point)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **\_make\_custom\_tooltip**(for\_text:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_private_method__make_custom_tooltip>`

Virtual method to be implemented by the user. Returns a **Control** node
that should be used as a tooltip instead of the default one. The
`for_text` includes the contents of the
`tooltip_text<class_Control_property_tooltip_text>` property.

The returned node must be of type **Control** or Control-derived. It can
have child nodes of any type. It is freed when the tooltip disappears,
so make sure you always provide a new instance (if you want to use a
pre-existing node from your scene tree, you can duplicate it and pass
the duplicated instance). When `null` or a non-Control node is returned,
the default tooltip will be used instead.

The returned node will be added as child to a
`PopupPanel<class_PopupPanel>`, so you should only provide the contents
of that panel. That `PopupPanel<class_PopupPanel>` can be themed using
`Theme.set_stylebox<class_Theme_method_set_stylebox>` for the type
`"TooltipPanel"` (see
`tooltip_text<class_Control_property_tooltip_text>` for an example).

\*\*Note:\*\* The tooltip is shrunk to minimal size. If you want to
ensure it's fully visible, you might want to set its
`custom_minimum_size<class_Control_property_custom_minimum_size>` to
some non-zero value.

\*\*Note:\*\* The node (and any relevant children) should be
`CanvasItem.visible<class_CanvasItem_property_visible>` when returned,
otherwise, the viewport that instantiates it will not be able to
calculate its minimum size reliably.

\*\*Example of usage with a custom-constructed node:\*\*

gdscript

func \_make\_custom\_tooltip(for\_text):  
var label = Label.new() label.text = for\_text return label

csharp

public override Control \_MakeCustomTooltip(string forText) { var label
= new Label(); label.Text = forText; return label; }

\*\*Example of usage with a custom scene instance:\*\*

gdscript

func \_make\_custom\_tooltip(for\_text):  
var tooltip = preload("<res://some_tooltip_scene.tscn>").instantiate()
tooltip.get\_node("Label").text = for\_text return tooltip

csharp

public override Control \_MakeCustomTooltip(string forText) { Node
tooltip =
ResourceLoader.Load&lt;PackedScene&gt;("<res://some_tooltip_scene.tscn>").Instantiate();
tooltip.GetNode&lt;Label&gt;("Label").Text = forText; return tooltip; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector3i<class_Vector3i>`\]
**\_structured\_text\_parser**(args: `Array<class_Array>`, text:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_private_method__structured_text_parser>`

User defined BiDi algorithm override function.

Returns an `Array<class_Array>` of `Vector3i<class_Vector3i>` text
ranges and text base directions, in the left-to-right order. Ranges
should cover full source `text` without overlaps. BiDi algorithm will be
used on each range separately.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **accept\_event**()
`🔗<class_Control_method_accept_event>`

Marks an input event as handled. Once you accept an input event, it
stops propagating, even to nodes listening to
`Node._unhandled_input<class_Node_private_method__unhandled_input>` or
`Node._unhandled_key_input<class_Node_private_method__unhandled_key_input>`.

\*\*Note:\*\* This does not affect the methods in `Input<class_Input>`,
only the way events are propagated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_color\_override**(name:
`StringName<class_StringName>`, color: `Color<class_Color>`)
`🔗<class_Control_method_add_theme_color_override>`

Creates a local override for a theme `Color<class_Color>` with the
specified `name`. Local overrides always take precedence when fetching
theme items for the control. An override can be removed with
`remove_theme_color_override<class_Control_method_remove_theme_color_override>`.

See also `get_theme_color<class_Control_method_get_theme_color>`.

\*\*Example of overriding a label's color and resetting it later:\*\*

gdscript

\# Given the child Label node "MyLabel", override its font color with a
custom value. $MyLabel.add\_theme\_color\_override("font\_color",
Color(1, 0.5, 0)) \# Reset the font color of the child label.
$MyLabel.remove\_theme\_color\_override("font\_color") \# Alternatively
it can be overridden with the default value from the Label type.
$MyLabel.add\_theme\_color\_override("font\_color",
get\_theme\_color("font\_color", "Label"))

csharp

// Given the child Label node "MyLabel", override its font color with a
custom value.
GetNode&lt;Label&gt;("MyLabel").AddThemeColorOverride("font\_color", new
Color(1, 0.5f, 0)); // Reset the font color of the child label.
GetNode&lt;Label&gt;("MyLabel").RemoveThemeColorOverride("font\_color");
// Alternatively it can be overridden with the default value from the
Label type.
GetNode&lt;Label&gt;("MyLabel").AddThemeColorOverride("font\_color",
GetThemeColor("font\_color", "Label"));

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_constant\_override**(name:
`StringName<class_StringName>`, constant: `int<class_int>`)
`🔗<class_Control_method_add_theme_constant_override>`

Creates a local override for a theme constant with the specified `name`.
Local overrides always take precedence when fetching theme items for the
control. An override can be removed with
`remove_theme_constant_override<class_Control_method_remove_theme_constant_override>`.

See also `get_theme_constant<class_Control_method_get_theme_constant>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_font\_override**(name:
`StringName<class_StringName>`, font: `Font<class_Font>`)
`🔗<class_Control_method_add_theme_font_override>`

Creates a local override for a theme `Font<class_Font>` with the
specified `name`. Local overrides always take precedence when fetching
theme items for the control. An override can be removed with
`remove_theme_font_override<class_Control_method_remove_theme_font_override>`.

See also `get_theme_font<class_Control_method_get_theme_font>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_font\_size\_override**(name:
`StringName<class_StringName>`, font\_size: `int<class_int>`)
`🔗<class_Control_method_add_theme_font_size_override>`

Creates a local override for a theme font size with the specified
`name`. Local overrides always take precedence when fetching theme items
for the control. An override can be removed with
`remove_theme_font_size_override<class_Control_method_remove_theme_font_size_override>`.

See also
`get_theme_font_size<class_Control_method_get_theme_font_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_icon\_override**(name:
`StringName<class_StringName>`, texture: `Texture2D<class_Texture2D>`)
`🔗<class_Control_method_add_theme_icon_override>`

Creates a local override for a theme icon with the specified `name`.
Local overrides always take precedence when fetching theme items for the
control. An override can be removed with
`remove_theme_icon_override<class_Control_method_remove_theme_icon_override>`.

See also `get_theme_icon<class_Control_method_get_theme_icon>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_theme\_stylebox\_override**(name:
`StringName<class_StringName>`, stylebox: `StyleBox<class_StyleBox>`)
`🔗<class_Control_method_add_theme_stylebox_override>`

Creates a local override for a theme `StyleBox<class_StyleBox>` with the
specified `name`. Local overrides always take precedence when fetching
theme items for the control. An override can be removed with
`remove_theme_stylebox_override<class_Control_method_remove_theme_stylebox_override>`.

See also `get_theme_stylebox<class_Control_method_get_theme_stylebox>`.

\*\*Example of modifying a property in a StyleBox by duplicating it:\*\*

gdscript

\# The snippet below assumes the child node MyButton has a StyleBoxFlat
assigned. \# Resources are shared across instances, so we need to
duplicate it \# to avoid modifying the appearance of all other buttons.
var new\_stylebox\_normal =
$MyButton.get\_theme\_stylebox("normal").duplicate()
new\_stylebox\_normal.border\_width\_top = 3
new\_stylebox\_normal.border\_color = Color(0, 1, 0.5)
$MyButton.add\_theme\_stylebox\_override("normal",
new\_stylebox\_normal) \# Remove the stylebox override.
$MyButton.remove\_theme\_stylebox\_override("normal")

csharp

// The snippet below assumes the child node MyButton has a StyleBoxFlat
assigned. // Resources are shared across instances, so we need to
duplicate it // to avoid modifying the appearance of all other buttons.
StyleBoxFlat newStyleboxNormal =
GetNode&lt;Button&gt;("MyButton").GetThemeStylebox("normal").Duplicate()
as StyleBoxFlat; newStyleboxNormal.BorderWidthTop = 3;
newStyleboxNormal.BorderColor = new Color(0, 1, 0.5f);
GetNode&lt;Button&gt;("MyButton").AddThemeStyleboxOverride("normal",
newStyleboxNormal); // Remove the stylebox override.
GetNode&lt;Button&gt;("MyButton").RemoveThemeStyleboxOverride("normal");

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **begin\_bulk\_theme\_override**()
`🔗<class_Control_method_begin_bulk_theme_override>`

Prevents `*_theme_*_override` methods from emitting
`NOTIFICATION_THEME_CHANGED<class_Control_constant_NOTIFICATION_THEME_CHANGED>`
until
`end_bulk_theme_override<class_Control_method_end_bulk_theme_override>`
is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **end\_bulk\_theme\_override**()
`🔗<class_Control_method_end_bulk_theme_override>`

Ends a bulk theme override update. See
`begin_bulk_theme_override<class_Control_method_begin_bulk_theme_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **find\_next\_valid\_focus**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_find_next_valid_focus>`

Finds the next (below in the tree) **Control** that can receive the
focus.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **find\_prev\_valid\_focus**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_find_prev_valid_focus>`

Finds the previous (above in the tree) **Control** that can receive the
focus.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **find\_valid\_focus\_neighbor**(side:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_find_valid_focus_neighbor>`

Finds the next **Control** that can receive the focus on the specified
`Side<enum_@GlobalScope_Side>`.

\*\*Note:\*\* This is different from
`get_focus_neighbor<class_Control_method_get_focus_neighbor>`, which
returns the path of a specified focus neighbor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_drag**(data:
`Variant<class_Variant>`, preview: `Control<class_Control>`)
`🔗<class_Control_method_force_drag>`

Forces drag and bypasses
`_get_drag_data<class_Control_private_method__get_drag_data>` and
`set_drag_preview<class_Control_method_set_drag_preview>` by passing
`data` and `preview`. Drag will start even if the mouse is neither over
nor pressed on this control.

The methods
`_can_drop_data<class_Control_private_method__can_drop_data>` and
`_drop_data<class_Control_private_method__drop_data>` must be
implemented on controls that want to receive drop data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_anchor**(side:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_anchor>`

Returns the anchor for the specified `Side<enum_@GlobalScope_Side>`. A
getter method for `anchor_bottom<class_Control_property_anchor_bottom>`,
`anchor_left<class_Control_property_anchor_left>`,
`anchor_right<class_Control_property_anchor_right>` and
`anchor_top<class_Control_property_anchor_top>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_begin**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_begin>`

Returns `offset_left<class_Control_property_offset_left>` and
`offset_top<class_Control_property_offset_top>`. See also
`position<class_Control_property_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_combined\_minimum\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_combined_minimum_size>`

Returns combined minimum size from
`custom_minimum_size<class_Control_property_custom_minimum_size>` and
`get_minimum_size<class_Control_method_get_minimum_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CursorShape<enum_Control_CursorShape>` **get\_cursor\_shape**(position:
`Vector2<class_Vector2>` = Vector2(0, 0))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_cursor_shape>`

Returns the mouse cursor shape the control displays on mouse hover. See
`CursorShape<enum_Control_CursorShape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_end**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_end>`

Returns `offset_right<class_Control_property_offset_right>` and
`offset_bottom<class_Control_property_offset_bottom>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_focus\_neighbor**(side:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_focus_neighbor>`

Returns the focus neighbor for the specified
`Side<enum_@GlobalScope_Side>`. A getter method for
`focus_neighbor_bottom<class_Control_property_focus_neighbor_bottom>`,
`focus_neighbor_left<class_Control_property_focus_neighbor_left>`,
`focus_neighbor_right<class_Control_property_focus_neighbor_right>` and
`focus_neighbor_top<class_Control_property_focus_neighbor_top>`.

\*\*Note:\*\* To find the next **Control** on the specific
`Side<enum_@GlobalScope_Side>`, even if a neighbor is not assigned, use
`find_valid_focus_neighbor<class_Control_method_find_valid_focus_neighbor>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_global\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_global_rect>`

Returns the position and size of the control relative to the containing
canvas. See `global_position<class_Control_property_global_position>`
and `size<class_Control_property_size>`.

\*\*Note:\*\* If the node itself or any parent
`CanvasItem<class_CanvasItem>` between the node and the canvas have a
non default rotation or skew, the resulting size is likely not
meaningful.

\*\*Note:\*\* Setting
`Viewport.gui_snap_controls_to_pixels<class_Viewport_property_gui_snap_controls_to_pixels>`
to `true` can lead to rounding inaccuracies between the displayed
control and the returned `Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_minimum\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_minimum_size>`

Returns the minimum size for this control. See
`custom_minimum_size<class_Control_property_custom_minimum_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_offset**(offset:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_offset>`

Returns the offset for the specified `Side<enum_@GlobalScope_Side>`. A
getter method for `offset_bottom<class_Control_property_offset_bottom>`,
`offset_left<class_Control_property_offset_left>`,
`offset_right<class_Control_property_offset_right>` and
`offset_top<class_Control_property_offset_top>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_parent\_area\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_parent_area_size>`

Returns the width/height occupied in the parent control.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **get\_parent\_control**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_parent_control>`

Returns the parent control node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_rect>`

Returns the position and size of the control in the coordinate system of
the containing node. See `position<class_Control_property_position>`,
`scale<class_Control_property_scale>` and
`size<class_Control_property_size>`.

\*\*Note:\*\* If `rotation<class_Control_property_rotation>` is not the
default rotation, the resulting size is not meaningful.

\*\*Note:\*\* Setting
`Viewport.gui_snap_controls_to_pixels<class_Viewport_property_gui_snap_controls_to_pixels>`
to `true` can lead to rounding inaccuracies between the displayed
control and the returned `Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_screen\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_screen_position>`

Returns the position of this **Control** in global screen coordinates
(i.e. taking window position into account). Mostly useful for editor
plugins.

Equals to `global_position<class_Control_property_global_position>` if
the window is embedded (see
`Viewport.gui_embed_subwindows<class_Viewport_property_gui_embed_subwindows>`).

\*\*Example usage for showing a popup:\*\*

    popup_menu.position = get_screen_position() + get_local_mouse_position()
    popup_menu.reset_size()
    popup_menu.popup()

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_theme\_color**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_color>`

Returns a `Color<class_Color>` from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
color item with the specified `name` and `theme_type`. If `theme_type`
is omitted the class name of the current control is used as the type, or
`theme_type_variation<class_Control_property_theme_type_variation>` if
it is defined. If the type is a class name its parent classes are also
checked, in order of inheritance. If the type is a variation its base
types are checked, in order of dependency, then the control's class name
and its parent classes are checked.

For the current control its local overrides are considered first (see
`add_theme_color_override<class_Control_method_add_theme_color_override>`),
then its assigned `theme<class_Control_property_theme>`. After the
current control, each parent control and its assigned
`theme<class_Control_property_theme>` are considered; controls without a
`theme<class_Control_property_theme>` assigned are skipped. If no
matching `Theme<class_Theme>` is found in the tree, the custom project
`Theme<class_Theme>` (see
`ProjectSettings.gui/theme/custom<class_ProjectSettings_property_gui/theme/custom>`)
and the default `Theme<class_Theme>` are used (see
`ThemeDB<class_ThemeDB>`).

gdscript

func \_ready():  
\# Get the font color defined for the current Control's class, if it
exists. modulate = get\_theme\_color("font\_color") \# Get the font
color defined for the Button class. modulate =
get\_theme\_color("font\_color", "Button")

csharp

public override void \_Ready() { // Get the font color defined for the
current Control's class, if it exists. Modulate =
GetThemeColor("font\_color"); // Get the font color defined for the
Button class. Modulate = GetThemeColor("font\_color", "Button"); }

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_theme\_constant**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_constant>`

Returns a constant from the first matching `Theme<class_Theme>` in the
tree if that `Theme<class_Theme>` has a constant item with the specified
`name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_theme\_default\_base\_scale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_default_base_scale>`

Returns the default base scale value from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
valid
`Theme.default_base_scale<class_Theme_property_default_base_scale>`
value.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Font<class_Font>` **get\_theme\_default\_font**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_default_font>`

Returns the default font from the first matching `Theme<class_Theme>` in
the tree if that `Theme<class_Theme>` has a valid
`Theme.default_font<class_Theme_property_default_font>` value.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_theme\_default\_font\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_default_font_size>`

Returns the default font size value from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
valid `Theme.default_font_size<class_Theme_property_default_font_size>`
value.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Font<class_Font>` **get\_theme\_font**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_font>`

Returns a `Font<class_Font>` from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a font
item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_theme\_font\_size**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_font_size>`

Returns a font size from the first matching `Theme<class_Theme>` in the
tree if that `Theme<class_Theme>` has a font size item with the
specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_theme\_icon**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_icon>`

Returns an icon from the first matching `Theme<class_Theme>` in the tree
if that `Theme<class_Theme>` has an icon item with the specified `name`
and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StyleBox<class_StyleBox>` **get\_theme\_stylebox**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_theme_stylebox>`

Returns a `StyleBox<class_StyleBox>` from the first matching
`Theme<class_Theme>` in the tree if that `Theme<class_Theme>` has a
stylebox item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tooltip**(at\_position:
`Vector2<class_Vector2>` = Vector2(0, 0))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_get_tooltip>`

Returns the tooltip text for the position `at_position` in control's
local coordinates, which will typically appear when the cursor is
resting over this control. By default, it returns
`tooltip_text<class_Control_property_tooltip_text>`.

This method can be overridden to customize its behavior. See
`_get_tooltip<class_Control_private_method__get_tooltip>`.

\*\*Note:\*\* If this method returns an empty `String<class_String>`, no
tooltip is displayed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **grab\_click\_focus**()
`🔗<class_Control_method_grab_click_focus>`

Creates an `InputEventMouseButton<class_InputEventMouseButton>` that
attempts to click the control. If the event is received, the control
acquires focus.

gdscript

func \_process(delta):  
grab\_click\_focus() \# When clicking another Control node, this node
will be clicked instead.

csharp

public override void \_Process(double delta) { GrabClickFocus(); // When
clicking another Control node, this node will be clicked instead. }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **grab\_focus**()
`🔗<class_Control_method_grab_focus>`

Steal the focus from another control and become the focused control (see
`focus_mode<class_Control_property_focus_mode>`).

\*\*Note:\*\* Using this method together with
`Callable.call_deferred<class_Callable_method_call_deferred>` makes it
more reliable, especially when called inside
`Node._ready<class_Node_private_method__ready>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_focus**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_focus>`

Returns `true` if this is the current focused control. See
`focus_mode<class_Control_property_focus_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_color**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_color>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a color item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_color\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_color_override>`

Returns `true` if there is a local override for a theme
`Color<class_Color>` with the specified `name` in this **Control** node.

See
`add_theme_color_override<class_Control_method_add_theme_color_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_constant**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_constant>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a constant item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_constant\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_constant_override>`

Returns `true` if there is a local override for a theme constant with
the specified `name` in this **Control** node.

See
`add_theme_constant_override<class_Control_method_add_theme_constant_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_font>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a font item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_font_override>`

Returns `true` if there is a local override for a theme
`Font<class_Font>` with the specified `name` in this **Control** node.

See
`add_theme_font_override<class_Control_method_add_theme_font_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font\_size**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_font_size>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a font size item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_font\_size\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_font_size_override>`

Returns `true` if there is a local override for a theme font size with
the specified `name` in this **Control** node.

See
`add_theme_font_size_override<class_Control_method_add_theme_font_size_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_icon**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_icon>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has an icon item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_icon\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_icon_override>`

Returns `true` if there is a local override for a theme icon with the
specified `name` in this **Control** node.

See
`add_theme_icon_override<class_Control_method_add_theme_icon_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_stylebox**(name:
`StringName<class_StringName>`, theme\_type:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_stylebox>`

Returns `true` if there is a matching `Theme<class_Theme>` in the tree
that has a stylebox item with the specified `name` and `theme_type`.

See `get_theme_color<class_Control_method_get_theme_color>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_theme\_stylebox\_override**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_has_theme_stylebox_override>`

Returns `true` if there is a local override for a theme
`StyleBox<class_StyleBox>` with the specified `name` in this **Control**
node.

See
`add_theme_stylebox_override<class_Control_method_add_theme_stylebox_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_drag\_successful**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_is_drag_successful>`

Returns `true` if a drag operation is successful. Alternative to
`Viewport.gui_is_drag_successful<class_Viewport_method_gui_is_drag_successful>`.

Best used with
`Node.NOTIFICATION_DRAG_END<class_Node_constant_NOTIFICATION_DRAG_END>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_layout\_rtl**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Control_method_is_layout_rtl>`

Returns `true` if layout is right-to-left.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **release\_focus**()
`🔗<class_Control_method_release_focus>`

Give up the focus. No other control will be able to receive input.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_color\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Control_method_remove_theme_color_override>`

Removes a local override for a theme `Color<class_Color>` with the
specified `name` previously added by
`add_theme_color_override<class_Control_method_add_theme_color_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_constant\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Control_method_remove_theme_constant_override>`

Removes a local override for a theme constant with the specified `name`
previously added by
`add_theme_constant_override<class_Control_method_add_theme_constant_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_font\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Control_method_remove_theme_font_override>`

Removes a local override for a theme `Font<class_Font>` with the
specified `name` previously added by
`add_theme_font_override<class_Control_method_add_theme_font_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_font\_size\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Control_method_remove_theme_font_size_override>`

Removes a local override for a theme font size with the specified `name`
previously added by
`add_theme_font_size_override<class_Control_method_add_theme_font_size_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_icon\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Control_method_remove_theme_icon_override>`

Removes a local override for a theme icon with the specified `name`
previously added by
`add_theme_icon_override<class_Control_method_add_theme_icon_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_theme\_stylebox\_override**(name:
`StringName<class_StringName>`)
`🔗<class_Control_method_remove_theme_stylebox_override>`

Removes a local override for a theme `StyleBox<class_StyleBox>` with the
specified `name` previously added by
`add_theme_stylebox_override<class_Control_method_add_theme_stylebox_override>`
or via the Inspector dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset\_size**()
`🔗<class_Control_method_reset_size>`

Resets the size to
`get_combined_minimum_size<class_Control_method_get_combined_minimum_size>`.
This is equivalent to calling `set_size(Vector2())` (or any size below
the minimum).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_anchor**(side:
`Side<enum_@GlobalScope_Side>`, anchor: `float<class_float>`,
keep\_offset: `bool<class_bool>` = false, push\_opposite\_anchor:
`bool<class_bool>` = true) `🔗<class_Control_method_set_anchor>`

Sets the anchor for the specified `Side<enum_@GlobalScope_Side>` to
`anchor`. A setter method for
`anchor_bottom<class_Control_property_anchor_bottom>`,
`anchor_left<class_Control_property_anchor_left>`,
`anchor_right<class_Control_property_anchor_right>` and
`anchor_top<class_Control_property_anchor_top>`.

If `keep_offset` is `true`, offsets aren't updated after this operation.

If `push_opposite_anchor` is `true` and the opposite anchor overlaps
this anchor, the opposite one will have its value overridden. For
example, when setting left anchor to 1 and the right anchor has value of
0.5, the right anchor will also get value of 1. If
`push_opposite_anchor` was `false`, the left anchor would get value 0.5.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_anchor\_and\_offset**(side:
`Side<enum_@GlobalScope_Side>`, anchor: `float<class_float>`, offset:
`float<class_float>`, push\_opposite\_anchor: `bool<class_bool>` =
false) `🔗<class_Control_method_set_anchor_and_offset>`

Works the same as `set_anchor<class_Control_method_set_anchor>`, but
instead of `keep_offset` argument and automatic update of offset, it
allows to set the offset yourself (see
`set_offset<class_Control_method_set_offset>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_anchors\_and\_offsets\_preset**(preset:
`LayoutPreset<enum_Control_LayoutPreset>`, resize\_mode:
`LayoutPresetMode<enum_Control_LayoutPresetMode>` = 0, margin:
`int<class_int>` = 0)
`🔗<class_Control_method_set_anchors_and_offsets_preset>`

Sets both anchor preset and offset preset. See
`set_anchors_preset<class_Control_method_set_anchors_preset>` and
`set_offsets_preset<class_Control_method_set_offsets_preset>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_anchors\_preset**(preset:
`LayoutPreset<enum_Control_LayoutPreset>`, keep\_offsets:
`bool<class_bool>` = false)
`🔗<class_Control_method_set_anchors_preset>`

Sets the anchors to a `preset` from
`LayoutPreset<enum_Control_LayoutPreset>` enum. This is the code
equivalent to using the Layout menu in the 2D editor.

If `keep_offsets` is `true`, control's position will also be updated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_begin**(position:
`Vector2<class_Vector2>`) `🔗<class_Control_method_set_begin>`

Sets `offset_left<class_Control_property_offset_left>` and
`offset_top<class_Control_property_offset_top>` at the same time.
Equivalent of changing `position<class_Control_property_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_drag\_forwarding**(drag\_func:
`Callable<class_Callable>`, can\_drop\_func: `Callable<class_Callable>`,
drop\_func: `Callable<class_Callable>`)
`🔗<class_Control_method_set_drag_forwarding>`

Forwards the handling of this control's
`_get_drag_data<class_Control_private_method__get_drag_data>`,
`_can_drop_data<class_Control_private_method__can_drop_data>` and
`_drop_data<class_Control_private_method__drop_data>` virtual functions
to delegate callables.

For each argument, if not empty, the delegate callable is used,
otherwise the local (virtual) function is used.

The function format for each callable should be exactly the same as the
virtual functions described above.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_drag\_preview**(control:
`Control<class_Control>`) `🔗<class_Control_method_set_drag_preview>`

Shows the given control at the mouse pointer. A good time to call this
method is in
`_get_drag_data<class_Control_private_method__get_drag_data>`. The
control must not be in the scene tree. You should not free the control,
and you should not keep a reference to the control beyond the duration
of the drag. It will be deleted automatically after the drag has ended.

gdscript

@export var color = Color(1, 0, 0, 1)

func \_get\_drag\_data(position):  
\# Use a control that is not in the tree var cpb =
ColorPickerButton.new() cpb.color = color cpb.size = Vector2(50, 50)
set\_drag\_preview(cpb) return color

csharp

\[Export\] private Color \_color = new Color(1, 0, 0, 1);

public override Variant \_GetDragData(Vector2 atPosition) { // Use a
control that is not in the tree var cpb = new ColorPickerButton();
cpb.Color = \_color; cpb.Size = new Vector2(50, 50);
SetDragPreview(cpb); return \_color; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_end**(position:
`Vector2<class_Vector2>`) `🔗<class_Control_method_set_end>`

Sets `offset_right<class_Control_property_offset_right>` and
`offset_bottom<class_Control_property_offset_bottom>` at the same time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_focus\_neighbor**(side:
`Side<enum_@GlobalScope_Side>`, neighbor: `NodePath<class_NodePath>`)
`🔗<class_Control_method_set_focus_neighbor>`

Sets the focus neighbor for the specified `Side<enum_@GlobalScope_Side>`
to the **Control** at `neighbor` node path. A setter method for
`focus_neighbor_bottom<class_Control_property_focus_neighbor_bottom>`,
`focus_neighbor_left<class_Control_property_focus_neighbor_left>`,
`focus_neighbor_right<class_Control_property_focus_neighbor_right>` and
`focus_neighbor_top<class_Control_property_focus_neighbor_top>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_global\_position**(position:
`Vector2<class_Vector2>`, keep\_offsets: `bool<class_bool>` = false)
`🔗<class_Control_method_set_global_position>`

Sets the `global_position<class_Control_property_global_position>` to
given `position`.

If `keep_offsets` is `true`, control's anchors will be updated instead
of offsets.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_offset**(side:
`Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
`🔗<class_Control_method_set_offset>`

Sets the offset for the specified `Side<enum_@GlobalScope_Side>` to
`offset`. A setter method for
`offset_bottom<class_Control_property_offset_bottom>`,
`offset_left<class_Control_property_offset_left>`,
`offset_right<class_Control_property_offset_right>` and
`offset_top<class_Control_property_offset_top>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_offsets\_preset**(preset:
`LayoutPreset<enum_Control_LayoutPreset>`, resize\_mode:
`LayoutPresetMode<enum_Control_LayoutPresetMode>` = 0, margin:
`int<class_int>` = 0) `🔗<class_Control_method_set_offsets_preset>`

Sets the offsets to a `preset` from
`LayoutPreset<enum_Control_LayoutPreset>` enum. This is the code
equivalent to using the Layout menu in the 2D editor.

Use parameter `resize_mode` with constants from
`LayoutPresetMode<enum_Control_LayoutPresetMode>` to better determine
the resulting size of the **Control**. Constant size will be ignored if
used with presets that change size, e.g.
`PRESET_LEFT_WIDE<class_Control_constant_PRESET_LEFT_WIDE>`.

Use parameter `margin` to determine the gap between the **Control** and
the edges.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_position**(position:
`Vector2<class_Vector2>`, keep\_offsets: `bool<class_bool>` = false)
`🔗<class_Control_method_set_position>`

Sets the `position<class_Control_property_position>` to given
`position`.

If `keep_offsets` is `true`, control's anchors will be updated instead
of offsets.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_size**(size: `Vector2<class_Vector2>`,
keep\_offsets: `bool<class_bool>` = false)
`🔗<class_Control_method_set_size>`

Sets the size (see `size<class_Control_property_size>`).

If `keep_offsets` is `true`, control's anchors will be updated instead
of offsets.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_minimum\_size**()
`🔗<class_Control_method_update_minimum_size>`

Invalidates the size cache in this node and in parent nodes up to top
level. Intended to be used with
`get_minimum_size<class_Control_method_get_minimum_size>` when the
return value is changed. Setting
`custom_minimum_size<class_Control_property_custom_minimum_size>`
directly calls this method automatically.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **warp\_mouse**(position:
`Vector2<class_Vector2>`) `🔗<class_Control_method_warp_mouse>`

Moves the mouse cursor to `position`, relative to
`position<class_Control_property_position>` of this **Control**.

\*\*Note:\*\* `warp_mouse<class_Control_method_warp_mouse>` is only
supported on Windows, macOS and Linux. It has no effect on Android, iOS
and Web.
