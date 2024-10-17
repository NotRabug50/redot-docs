github\_url  
hide

# GraphEdit

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

An editor for graph-like structures, using
`GraphNode<class_GraphNode>`s.

classref-introduction-group

## Description

**GraphEdit** provides tools for creation, manipulation, and display of
various graphs. Its main purpose in the engine is to power the visual
programming systems, such as visual shaders, but it is also available
for use in user projects.

\*\*GraphEdit\*\* by itself is only an empty container, representing an
infinite grid where `GraphNode<class_GraphNode>`s can be placed. Each
`GraphNode<class_GraphNode>` represents a node in the graph, a single
unit of data in the connected scheme. **GraphEdit**, in turn, helps to
control various interactions with nodes and between nodes. When the user
attempts to connect, disconnect, or delete a
`GraphNode<class_GraphNode>`, a signal is emitted in the **GraphEdit**,
but no action is taken by default. It is the responsibility of the
programmer utilizing this control to implement the necessary logic to
determine how each request should be handled.

\*\*Performance:\*\* It is greatly advised to enable low-processor usage
mode (see
`OS.low_processor_usage_mode<class_OS_property_low_processor_usage_mode>`)
when using GraphEdits.

\*\*Note:\*\* Keep in mind that
`Node.get_children<class_Node_method_get_children>` will also return the
connection layer node named `_connection_layer` due to technical
limitations. This behavior may change in future releases.

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
<tr>
</tr>
<tr>
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

**begin\_node\_move**() `🔗<class_GraphEdit_signal_begin_node_move>`

Emitted at the beginning of a `GraphElement<class_GraphElement>`'s
movement.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**connection\_drag\_ended**()
`🔗<class_GraphEdit_signal_connection_drag_ended>`

Emitted at the end of a connection drag.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**connection\_drag\_started**(from\_node:
`StringName<class_StringName>`, from\_port: `int<class_int>`,
is\_output: `bool<class_bool>`)
`🔗<class_GraphEdit_signal_connection_drag_started>`

Emitted at the beginning of a connection drag.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**connection\_from\_empty**(to\_node: `StringName<class_StringName>`,
to\_port: `int<class_int>`, release\_position: `Vector2<class_Vector2>`)
`🔗<class_GraphEdit_signal_connection_from_empty>`

Emitted when user drags a connection from an input port into the empty
space of the graph.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**connection\_request**(from\_node: `StringName<class_StringName>`,
from\_port: `int<class_int>`, to\_node: `StringName<class_StringName>`,
to\_port: `int<class_int>`)
`🔗<class_GraphEdit_signal_connection_request>`

Emitted to the GraphEdit when the connection between the `from_port` of
the `from_node` `GraphNode<class_GraphNode>` and the `to_port` of the
`to_node` `GraphNode<class_GraphNode>` is attempted to be created.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**connection\_to\_empty**(from\_node: `StringName<class_StringName>`,
from\_port: `int<class_int>`, release\_position:
`Vector2<class_Vector2>`)
`🔗<class_GraphEdit_signal_connection_to_empty>`

Emitted when user drags a connection from an output port into the empty
space of the graph.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**copy\_nodes\_request**()
`🔗<class_GraphEdit_signal_copy_nodes_request>`

Emitted when this **GraphEdit** captures a `ui_copy` action (`Ctrl + C`
by default). In general, this signal indicates that the selected
`GraphElement<class_GraphElement>`s should be copied.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**cut\_nodes\_request**() `🔗<class_GraphEdit_signal_cut_nodes_request>`

Emitted when this **GraphEdit** captures a `ui_cut` action (`Ctrl + X`
by default). In general, this signal indicates that the selected
`GraphElement<class_GraphElement>`s should be cut.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**delete\_nodes\_request**(nodes:
`Array<class_Array>`\[`StringName<class_StringName>`\])
`🔗<class_GraphEdit_signal_delete_nodes_request>`

Emitted when this **GraphEdit** captures a `ui_graph_delete` action
(`Delete` by default).

`nodes` is an array of node names that should be removed. These usually
include all selected nodes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**disconnection\_request**(from\_node: `StringName<class_StringName>`,
from\_port: `int<class_int>`, to\_node: `StringName<class_StringName>`,
to\_port: `int<class_int>`)
`🔗<class_GraphEdit_signal_disconnection_request>`

Emitted to the GraphEdit when the connection between `from_port` of
`from_node` `GraphNode<class_GraphNode>` and `to_port` of `to_node`
`GraphNode<class_GraphNode>` is attempted to be removed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**duplicate\_nodes\_request**()
`🔗<class_GraphEdit_signal_duplicate_nodes_request>`

Emitted when this **GraphEdit** captures a `ui_graph_duplicate` action
(`Ctrl + D` by default). In general, this signal indicates that the
selected `GraphElement<class_GraphElement>`s should be duplicated.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**end\_node\_move**() `🔗<class_GraphEdit_signal_end_node_move>`

Emitted at the end of a `GraphElement<class_GraphElement>`'s movement.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**frame\_rect\_changed**(frame: `GraphFrame<class_GraphFrame>`,
new\_rect: `Vector2<class_Vector2>`)
`🔗<class_GraphEdit_signal_frame_rect_changed>`

Emitted when the `GraphFrame<class_GraphFrame>` `frame` is resized to
`new_rect`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**graph\_elements\_linked\_to\_frame\_request**(elements:
`Array<class_Array>`, frame: `StringName<class_StringName>`)
`🔗<class_GraphEdit_signal_graph_elements_linked_to_frame_request>`

Emitted when one or more `GraphElement<class_GraphElement>`s are dropped
onto the `GraphFrame<class_GraphFrame>` named `frame`, when they were
not previously attached to any other one.

`elements` is an array of `GraphElement<class_GraphElement>`s to be
attached.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_deselected**(node: `Node<class_Node>`)
`🔗<class_GraphEdit_signal_node_deselected>`

Emitted when the given `GraphElement<class_GraphElement>` node is
deselected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_selected**(node: `Node<class_Node>`)
`🔗<class_GraphEdit_signal_node_selected>`

Emitted when the given `GraphElement<class_GraphElement>` node is
selected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**paste\_nodes\_request**()
`🔗<class_GraphEdit_signal_paste_nodes_request>`

Emitted when this **GraphEdit** captures a `ui_paste` action (`Ctrl + V`
by default). In general, this signal indicates that previously copied
`GraphElement<class_GraphElement>`s should be pasted.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**popup\_request**(at\_position: `Vector2<class_Vector2>`)
`🔗<class_GraphEdit_signal_popup_request>`

Emitted when a popup is requested. Happens on right-clicking in the
GraphEdit. `at_position` is the position of the mouse pointer when the
signal is sent.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**scroll\_offset\_changed**(offset: `Vector2<class_Vector2>`)
`🔗<class_GraphEdit_signal_scroll_offset_changed>`

Emitted when the scroll offset is changed by the user. It will not be
emitted when changed in code.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **PanningScheme**: `🔗<enum_GraphEdit_PanningScheme>`

classref-enumeration-constant

`PanningScheme<enum_GraphEdit_PanningScheme>` **SCROLL\_ZOOMS** = `0`

`Mouse Wheel` will zoom, `Ctrl + Mouse Wheel` will move the view.

classref-enumeration-constant

`PanningScheme<enum_GraphEdit_PanningScheme>` **SCROLL\_PANS** = `1`

`Mouse Wheel` will move the view, `Ctrl + Mouse Wheel` will zoom.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GridPattern**: `🔗<enum_GraphEdit_GridPattern>`

classref-enumeration-constant

`GridPattern<enum_GraphEdit_GridPattern>` **GRID\_PATTERN\_LINES** = `0`

Draw the grid using solid lines.

classref-enumeration-constant

`GridPattern<enum_GraphEdit_GridPattern>` **GRID\_PATTERN\_DOTS** = `1`

Draw the grid using dots.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **connection\_lines\_antialiased** = `true`
`🔗<class_GraphEdit_property_connection_lines_antialiased>`

classref-property-setget

-   `void (No return value.)`
    **set\_connection\_lines\_antialiased**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_connection\_lines\_antialiased**()

If `true`, the lines between nodes will use antialiasing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **connection\_lines\_curvature** = `0.5`
`🔗<class_GraphEdit_property_connection_lines_curvature>`

classref-property-setget

-   `void (No return value.)`
    **set\_connection\_lines\_curvature**(value: `float<class_float>`)
-   `float<class_float>` **get\_connection\_lines\_curvature**()

The curvature of the lines between the nodes. 0 results in straight
lines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **connection\_lines\_thickness** = `4.0`
`🔗<class_GraphEdit_property_connection_lines_thickness>`

classref-property-setget

-   `void (No return value.)`
    **set\_connection\_lines\_thickness**(value: `float<class_float>`)
-   `float<class_float>` **get\_connection\_lines\_thickness**()

The thickness of the lines between the nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`GridPattern<enum_GraphEdit_GridPattern>` **grid\_pattern** = `0`
`🔗<class_GraphEdit_property_grid_pattern>`

classref-property-setget

-   `void (No return value.)` **set\_grid\_pattern**(value:
    `GridPattern<enum_GraphEdit_GridPattern>`)
-   `GridPattern<enum_GraphEdit_GridPattern>` **get\_grid\_pattern**()

The pattern used for drawing the grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **minimap\_enabled** = `true`
`🔗<class_GraphEdit_property_minimap_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_minimap\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_minimap\_enabled**()

If `true`, the minimap is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **minimap\_opacity** = `0.65`
`🔗<class_GraphEdit_property_minimap_opacity>`

classref-property-setget

-   `void (No return value.)` **set\_minimap\_opacity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_minimap\_opacity**()

The opacity of the minimap rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **minimap\_size** = `Vector2(240, 160)`
`🔗<class_GraphEdit_property_minimap_size>`

classref-property-setget

-   `void (No return value.)` **set\_minimap\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_minimap\_size**()

The size of the minimap rectangle. The map itself is based on the size
of the grid area and is scaled to fit this rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PanningScheme<enum_GraphEdit_PanningScheme>` **panning\_scheme** = `0`
`🔗<class_GraphEdit_property_panning_scheme>`

classref-property-setget

-   `void (No return value.)` **set\_panning\_scheme**(value:
    `PanningScheme<enum_GraphEdit_PanningScheme>`)
-   `PanningScheme<enum_GraphEdit_PanningScheme>`
    **get\_panning\_scheme**()

Defines the control scheme for panning with mouse wheel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **right\_disconnects** = `false`
`🔗<class_GraphEdit_property_right_disconnects>`

classref-property-setget

-   `void (No return value.)` **set\_right\_disconnects**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_right\_disconnects\_enabled**()

If `true`, enables disconnection of existing connections in the
GraphEdit by dragging the right end.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **scroll\_offset** = `Vector2(0, 0)`
`🔗<class_GraphEdit_property_scroll_offset>`

classref-property-setget

-   `void (No return value.)` **set\_scroll\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_scroll\_offset**()

The scroll offset.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_arrange\_button** = `true`
`🔗<class_GraphEdit_property_show_arrange_button>`

classref-property-setget

-   `void (No return value.)` **set\_show\_arrange\_button**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_arrange\_button**()

If `true`, the button to automatically arrange graph nodes is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_grid** = `true`
`🔗<class_GraphEdit_property_show_grid>`

classref-property-setget

-   `void (No return value.)` **set\_show\_grid**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_grid**()

If `true`, the grid is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_grid\_buttons** = `true`
`🔗<class_GraphEdit_property_show_grid_buttons>`

classref-property-setget

-   `void (No return value.)` **set\_show\_grid\_buttons**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_grid\_buttons**()

If `true`, buttons that allow to configure grid and snapping options are
visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_menu** = `true`
`🔗<class_GraphEdit_property_show_menu>`

classref-property-setget

-   `void (No return value.)` **set\_show\_menu**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_menu**()

If `true`, the menu toolbar is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_minimap\_button** = `true`
`🔗<class_GraphEdit_property_show_minimap_button>`

classref-property-setget

-   `void (No return value.)` **set\_show\_minimap\_button**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_minimap\_button**()

If `true`, the button to toggle the minimap is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_zoom\_buttons** = `true`
`🔗<class_GraphEdit_property_show_zoom_buttons>`

classref-property-setget

-   `void (No return value.)` **set\_show\_zoom\_buttons**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_zoom\_buttons**()

If `true`, buttons that allow to change and reset the zoom level are
visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_zoom\_label** = `false`
`🔗<class_GraphEdit_property_show_zoom_label>`

classref-property-setget

-   `void (No return value.)` **set\_show\_zoom\_label**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_zoom\_label**()

If `true`, the label with the current zoom level is visible. The zoom
level is displayed in percents.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **snapping\_distance** = `20`
`🔗<class_GraphEdit_property_snapping_distance>`

classref-property-setget

-   `void (No return value.)` **set\_snapping\_distance**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_snapping\_distance**()

The snapping distance in pixels, also determines the grid line distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **snapping\_enabled** = `true`
`🔗<class_GraphEdit_property_snapping_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_snapping\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_snapping\_enabled**()

If `true`, enables snapping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **zoom** = `1.0`
`🔗<class_GraphEdit_property_zoom>`

classref-property-setget

-   `void (No return value.)` **set\_zoom**(value: `float<class_float>`)
-   `float<class_float>` **get\_zoom**()

The current zoom value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **zoom\_max** = `2.0736`
`🔗<class_GraphEdit_property_zoom_max>`

classref-property-setget

-   `void (No return value.)` **set\_zoom\_max**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_zoom\_max**()

The upper zoom limit.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **zoom\_min** = `0.232568`
`🔗<class_GraphEdit_property_zoom_min>`

classref-property-setget

-   `void (No return value.)` **set\_zoom\_min**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_zoom\_min**()

The lower zoom limit.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **zoom\_step** = `1.2`
`🔗<class_GraphEdit_property_zoom_step>`

classref-property-setget

-   `void (No return value.)` **set\_zoom\_step**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_zoom\_step**()

The step of each zoom level.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**\_get\_connection\_line**(from\_position: `Vector2<class_Vector2>`,
to\_position: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphEdit_private_method__get_connection_line>`

Virtual method which can be overridden to customize how connections are
drawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_in\_input\_hotzone**(in\_node:
`Object<class_Object>`, in\_port: `int<class_int>`, mouse\_position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GraphEdit_private_method__is_in_input_hotzone>`

Returns whether the `mouse_position` is in the input hot zone.

By default, a hot zone is a `Rect2<class_Rect2>` positioned such that
its center is at
`in_node`.`GraphNode.get_input_port_position<class_GraphNode_method_get_input_port_position>`(`in_port`)
(For output's case, call
`GraphNode.get_output_port_position<class_GraphNode_method_get_output_port_position>`
instead). The hot zone's width is twice the Theme Property
`port_grab_distance_horizontal`, and its height is twice the
`port_grab_distance_vertical`.

Below is a sample code to help get started:

    func _is_in_input_hotzone(in_node, in_port, mouse_position):
        var port_size: Vector2 = Vector2(get_theme_constant("port_grab_distance_horizontal"), get_theme_constant("port_grab_distance_vertical"))
        var port_pos: Vector2 = in_node.get_position() + in_node.get_input_port_position(in_port) - port_size / 2
        var rect = Rect2(port_pos, port_size)

        return rect.has_point(mouse_position)

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_in\_output\_hotzone**(in\_node:
`Object<class_Object>`, in\_port: `int<class_int>`, mouse\_position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GraphEdit_private_method__is_in_output_hotzone>`

Returns whether the `mouse_position` is in the output hot zone. For more
information on hot zones, see
`_is_in_input_hotzone<class_GraphEdit_private_method__is_in_input_hotzone>`.

Below is a sample code to help get started:

    func _is_in_output_hotzone(in_node, in_port, mouse_position):
        var port_size: Vector2 = Vector2(get_theme_constant("port_grab_distance_horizontal"), get_theme_constant("port_grab_distance_vertical"))
        var port_pos: Vector2 = in_node.get_position() + in_node.get_output_port_position(in_port) - port_size / 2
        var rect = Rect2(port_pos, port_size)

        return rect.has_point(mouse_position)

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_node\_hover\_valid**(from\_node:
`StringName<class_StringName>`, from\_port: `int<class_int>`, to\_node:
`StringName<class_StringName>`, to\_port: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GraphEdit_private_method__is_node_hover_valid>`

This virtual method can be used to insert additional error detection
while the user is dragging a connection over a valid port.

Return `true` if the connection is indeed valid or return `false` if the
connection is impossible. If the connection is impossible, no snapping
to the port and thus no connection request to that port will happen.

In this example a connection to same node is suppressed:

gdscript

func \_is\_node\_hover\_valid(from, from\_port, to, to\_port):  
return from != to

csharp

public override bool \_IsNodeHoverValid(StringName fromNode, int
fromPort, StringName toNode, int toPort) { return fromNode != toNode; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_valid\_connection\_type**(from\_type:
`int<class_int>`, to\_type: `int<class_int>`)
`🔗<class_GraphEdit_method_add_valid_connection_type>`

Allows the connection between two different port types. The port type is
defined individually for the left and the right port of each slot with
the `GraphNode.set_slot<class_GraphNode_method_set_slot>` method.

See also
`is_valid_connection_type<class_GraphEdit_method_is_valid_connection_type>`
and
`remove_valid_connection_type<class_GraphEdit_method_remove_valid_connection_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_valid\_left\_disconnect\_type**(type:
`int<class_int>`)
`🔗<class_GraphEdit_method_add_valid_left_disconnect_type>`

Allows to disconnect nodes when dragging from the left port of the
`GraphNode<class_GraphNode>`'s slot if it has the specified type. See
also
`remove_valid_left_disconnect_type<class_GraphEdit_method_remove_valid_left_disconnect_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_valid\_right\_disconnect\_type**(type:
`int<class_int>`)
`🔗<class_GraphEdit_method_add_valid_right_disconnect_type>`

Allows to disconnect nodes when dragging from the right port of the
`GraphNode<class_GraphNode>`'s slot if it has the specified type. See
also
`remove_valid_right_disconnect_type<class_GraphEdit_method_remove_valid_right_disconnect_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **arrange\_nodes**()
`🔗<class_GraphEdit_method_arrange_nodes>`

Rearranges selected nodes in a layout with minimum crossings between
connections and uniform horizontal and vertical gap between nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **attach\_graph\_element\_to\_frame**(element:
`StringName<class_StringName>`, frame: `StringName<class_StringName>`)
`🔗<class_GraphEdit_method_attach_graph_element_to_frame>`

Attaches the `element` `GraphElement<class_GraphElement>` to the `frame`
`GraphFrame<class_GraphFrame>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_connections**()
`🔗<class_GraphEdit_method_clear_connections>`

Removes all connections between nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_node**(from\_node:
`StringName<class_StringName>`, from\_port: `int<class_int>`, to\_node:
`StringName<class_StringName>`, to\_port: `int<class_int>`)
`🔗<class_GraphEdit_method_connect_node>`

Create a connection between the `from_port` of the `from_node`
`GraphNode<class_GraphNode>` and the `to_port` of the `to_node`
`GraphNode<class_GraphNode>`. If the connection already exists, no
connection is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**detach\_graph\_element\_from\_frame**(element:
`StringName<class_StringName>`)
`🔗<class_GraphEdit_method_detach_graph_element_from_frame>`

Detaches the `element` `GraphElement<class_GraphElement>` from the
`GraphFrame<class_GraphFrame>` it is currently attached to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_node**(from\_node:
`StringName<class_StringName>`, from\_port: `int<class_int>`, to\_node:
`StringName<class_StringName>`, to\_port: `int<class_int>`)
`🔗<class_GraphEdit_method_disconnect_node>`

Removes the connection between the `from_port` of the `from_node`
`GraphNode<class_GraphNode>` and the `to_port` of the `to_node`
`GraphNode<class_GraphNode>`. If the connection does not exist, no
connection is removed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_connection\_drag\_end**()
`🔗<class_GraphEdit_method_force_connection_drag_end>`

Ends the creation of the current connection. In other words, if you are
dragging a connection you can use this method to abort the process and
remove the line that followed your cursor.

This is best used together with
`connection_drag_started<class_GraphEdit_signal_connection_drag_started>`
and
`connection_drag_ended<class_GraphEdit_signal_connection_drag_ended>` to
add custom behavior like node addition through shortcuts.

\*\*Note:\*\* This method suppresses any other connection request
signals apart from
`connection_drag_ended<class_GraphEdit_signal_connection_drag_ended>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_attached\_nodes\_of\_frame**(frame:
`StringName<class_StringName>`)
`🔗<class_GraphEdit_method_get_attached_nodes_of_frame>`

Returns an array of node names that are attached to the
`GraphFrame<class_GraphFrame>` with the given name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**get\_closest\_connection\_at\_point**(point: `Vector2<class_Vector2>`,
max\_distance: `float<class_float>` = 4.0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphEdit_method_get_closest_connection_at_point>`

Returns the closest connection to the given point in screen space. If no
connection is found within `max_distance` pixels, an empty
`Dictionary<class_Dictionary>` is returned.

A connection consists in a structure of the form
`{ from_port: 0, from_node: "GraphNode name 0", to_port: 1, to_node: "GraphNode name 1" }`.

For example, getting a connection at a given mouse position can be
achieved like this:

gdscript

var connection =
get\_closest\_connection\_at\_point(mouse\_event.get\_position())

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_connection\_line**(from\_node: `Vector2<class_Vector2>`,
to\_node: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphEdit_method_get_connection_line>`

Returns the points which would make up a connection between `from_node`
and `to_node`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_connection\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphEdit_method_get_connection_list>`

Returns an `Array<class_Array>` containing the list of connections. A
connection consists in a structure of the form
`{ from_port: 0, from_node: "GraphNode name 0", to_port: 1, to_node: "GraphNode name 1" }`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_connections\_intersecting\_with\_rect**(rect:
`Rect2<class_Rect2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphEdit_method_get_connections_intersecting_with_rect>`

Returns an `Array<class_Array>` containing the list of connections that
intersect with the given `Rect2<class_Rect2>`. A connection consists in
a structure of the form
`{ from_port: 0, from_node: "GraphNode name 0", to_port: 1, to_node: "GraphNode name 1" }`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GraphFrame<class_GraphFrame>` **get\_element\_frame**(element:
`StringName<class_StringName>`)
`🔗<class_GraphEdit_method_get_element_frame>`

Returns the `GraphFrame<class_GraphFrame>` that contains the
`GraphElement<class_GraphElement>` with the given name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HBoxContainer<class_HBoxContainer>` **get\_menu\_hbox**()
`🔗<class_GraphEdit_method_get_menu_hbox>`

Gets the `HBoxContainer<class_HBoxContainer>` that contains the zooming
and grid snap controls in the top left of the graph. You can use this
method to reposition the toolbar or to add your own custom controls to
it.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_node\_connected**(from\_node:
`StringName<class_StringName>`, from\_port: `int<class_int>`, to\_node:
`StringName<class_StringName>`, to\_port: `int<class_int>`)
`🔗<class_GraphEdit_method_is_node_connected>`

Returns `true` if the `from_port` of the `from_node`
`GraphNode<class_GraphNode>` is connected to the `to_port` of the
`to_node` `GraphNode<class_GraphNode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_connection\_type**(from\_type:
`int<class_int>`, to\_type: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphEdit_method_is_valid_connection_type>`

Returns whether it's possible to make a connection between two different
port types. The port type is defined individually for the left and the
right port of each slot with the
`GraphNode.set_slot<class_GraphNode_method_set_slot>` method.

See also
`add_valid_connection_type<class_GraphEdit_method_add_valid_connection_type>`
and
`remove_valid_connection_type<class_GraphEdit_method_remove_valid_connection_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_valid\_connection\_type**(from\_type: `int<class_int>`,
to\_type: `int<class_int>`)
`🔗<class_GraphEdit_method_remove_valid_connection_type>`

Disallows the connection between two different port types previously
allowed by
`add_valid_connection_type<class_GraphEdit_method_add_valid_connection_type>`.
The port type is defined individually for the left and the right port of
each slot with the `GraphNode.set_slot<class_GraphNode_method_set_slot>`
method.

See also
`is_valid_connection_type<class_GraphEdit_method_is_valid_connection_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_valid\_left\_disconnect\_type**(type: `int<class_int>`)
`🔗<class_GraphEdit_method_remove_valid_left_disconnect_type>`

Disallows to disconnect nodes when dragging from the left port of the
`GraphNode<class_GraphNode>`'s slot if it has the specified type. Use
this to disable disconnection previously allowed with
`add_valid_left_disconnect_type<class_GraphEdit_method_add_valid_left_disconnect_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_valid\_right\_disconnect\_type**(type: `int<class_int>`)
`🔗<class_GraphEdit_method_remove_valid_right_disconnect_type>`

Disallows to disconnect nodes when dragging from the right port of the
`GraphNode<class_GraphNode>`'s slot if it has the specified type. Use
this to disable disconnection previously allowed with
`add_valid_right_disconnect_type<class_GraphEdit_method_add_valid_right_disconnect_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_connection\_activity**(from\_node:
`StringName<class_StringName>`, from\_port: `int<class_int>`, to\_node:
`StringName<class_StringName>`, to\_port: `int<class_int>`, amount:
`float<class_float>`)
`🔗<class_GraphEdit_method_set_connection_activity>`

Sets the coloration of the connection between `from_node`'s `from_port`
and `to_node`'s `to_port` with the color provided in the
`activity<class_GraphEdit_theme_color_activity>` theme property. The
color is linearly interpolated between the connection color and the
activity color using `amount` as weight.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_selected**(node: `Node<class_Node>`)
`🔗<class_GraphEdit_method_set_selected>`

Sets the specified `node` as the one selected.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **activity** = `Color(1, 1, 1, 1)`
`🔗<class_GraphEdit_theme_color_activity>`

Color the connection line is interpolated to based on the activity value
of a connection (see
`set_connection_activity<class_GraphEdit_method_set_connection_activity>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **connection\_hover\_tint\_color** =
`Color(0, 0, 0, 0.3)`
`🔗<class_GraphEdit_theme_color_connection_hover_tint_color>`

Color which is blended with the connection line when the mouse is
hovering over it.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **connection\_rim\_color** =
`Color(0.1, 0.1, 0.1, 0.6)`
`🔗<class_GraphEdit_theme_color_connection_rim_color>`

Color of the rim around each connection line used for making
intersecting lines more distinguishable.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **connection\_valid\_target\_tint\_color** =
`Color(1, 1, 1, 0.4)`
`🔗<class_GraphEdit_theme_color_connection_valid_target_tint_color>`

Color which is blended with the connection line when the currently
dragged connection is hovering over a valid target port.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **grid\_major** = `Color(1, 1, 1, 0.2)`
`🔗<class_GraphEdit_theme_color_grid_major>`

Color of major grid lines/dots.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **grid\_minor** = `Color(1, 1, 1, 0.05)`
`🔗<class_GraphEdit_theme_color_grid_minor>`

Color of minor grid lines/dots.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **selection\_fill** = `Color(1, 1, 1, 0.3)`
`🔗<class_GraphEdit_theme_color_selection_fill>`

The fill color of the selection rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **selection\_stroke** = `Color(1, 1, 1, 0.8)`
`🔗<class_GraphEdit_theme_color_selection_stroke>`

The outline color of the selection rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **port\_hotzone\_inner\_extent** = `22`
`🔗<class_GraphEdit_theme_constant_port_hotzone_inner_extent>`

The horizontal range within which a port can be grabbed (inner side).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **port\_hotzone\_outer\_extent** = `26`
`🔗<class_GraphEdit_theme_constant_port_hotzone_outer_extent>`

The horizontal range within which a port can be grabbed (outer side).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **grid\_toggle**
`🔗<class_GraphEdit_theme_icon_grid_toggle>`

The icon for the grid toggle button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **layout**
`🔗<class_GraphEdit_theme_icon_layout>`

The icon for the layout button for auto-arranging the graph.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **minimap\_toggle**
`🔗<class_GraphEdit_theme_icon_minimap_toggle>`

The icon for the minimap toggle button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **snapping\_toggle**
`🔗<class_GraphEdit_theme_icon_snapping_toggle>`

The icon for the snapping toggle button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **zoom\_in**
`🔗<class_GraphEdit_theme_icon_zoom_in>`

The icon for the zoom in button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **zoom\_out**
`🔗<class_GraphEdit_theme_icon_zoom_out>`

The icon for the zoom out button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **zoom\_reset**
`🔗<class_GraphEdit_theme_icon_zoom_reset>`

The icon for the zoom reset button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **menu\_panel**
`🔗<class_GraphEdit_theme_style_menu_panel>`

There is currently no description for this theme property. Please help
us by `contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **panel**
`🔗<class_GraphEdit_theme_style_panel>`

The background drawn under the grid.
