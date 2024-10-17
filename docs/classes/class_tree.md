github\_url  
hide

# Tree

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control used to show a set of internal `TreeItem<class_TreeItem>`s in
a hierarchical structure.

classref-introduction-group

## Description

A control used to show a set of internal `TreeItem<class_TreeItem>`s in
a hierarchical structure. The tree items can be selected, expanded and
collapsed. The tree can have multiple columns with custom controls like
`LineEdit<class_LineEdit>`s, buttons and popups. It can be useful for
structured displays and interactions.

Trees are built via code, using `TreeItem<class_TreeItem>` objects to
create the structure. They have a single root, but multiple roots can be
simulated with `hide_root<class_Tree_property_hide_root>`:

gdscript

func \_ready():  
var tree = Tree.new() var root = tree.create\_item() tree.hide\_root =
true var child1 = tree.create\_item(root) var child2 =
tree.create\_item(root) var subchild1 = tree.create\_item(child1)
subchild1.set\_text(0, "Subchild1")

csharp

public override void \_Ready() { var tree = new Tree(); TreeItem root =
tree.CreateItem(); tree.HideRoot = true; TreeItem child1 =
tree.CreateItem(root); TreeItem child2 = tree.CreateItem(root); TreeItem
subchild1 = tree.CreateItem(child1); subchild1.SetText(0, "Subchild1");
}

To iterate over all the `TreeItem<class_TreeItem>` objects in a **Tree**
object, use `TreeItem.get_next<class_TreeItem_method_get_next>` and
`TreeItem.get_first_child<class_TreeItem_method_get_first_child>` after
getting the root through `get_root<class_Tree_method_get_root>`. You can
use `Object.free<class_Object_method_free>` on a
`TreeItem<class_TreeItem>` to remove it from the **Tree**.

\*\*Incremental search:\*\* Like `ItemList<class_ItemList>` and
`PopupMenu<class_PopupMenu>`, **Tree** supports searching within the
list while the control is focused. Press a key that matches the first
letter of an item's name to select the first item starting with the
given letter. After that point, there are two ways to perform
incremental search: 1) Press the same key again before the timeout
duration to select the next item starting with the same letter. 2) Press
letter keys that match the rest of the word before the timeout duration
to match to select the item in question directly. Both of these actions
will be reset to the beginning of the list if the timeout duration has
passed since the last keystroke was registered. You can adjust the
timeout duration by changing
`ProjectSettings.gui/timers/incremental_search_max_interval_msec<class_ProjectSettings_property_gui/timers/incremental_search_max_interval_msec>`.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

**button\_clicked**(item: `TreeItem<class_TreeItem>`, column:
`int<class_int>`, id: `int<class_int>`, mouse\_button\_index:
`int<class_int>`) `🔗<class_Tree_signal_button_clicked>`

Emitted when a button on the tree was pressed (see
`TreeItem.add_button<class_TreeItem_method_add_button>`).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**cell\_selected**() `🔗<class_Tree_signal_cell_selected>`

Emitted when a cell is selected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**check\_propagated\_to\_item**(item: `TreeItem<class_TreeItem>`,
column: `int<class_int>`)
`🔗<class_Tree_signal_check_propagated_to_item>`

Emitted when
`TreeItem.propagate_check<class_TreeItem_method_propagate_check>` is
called. Connect to this signal to process the items that are affected
when `TreeItem.propagate_check<class_TreeItem_method_propagate_check>`
is invoked. The order that the items affected will be processed is as
follows: the item that invoked the method, children of that item, and
finally parents of that item.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**column\_title\_clicked**(column: `int<class_int>`,
mouse\_button\_index: `int<class_int>`)
`🔗<class_Tree_signal_column_title_clicked>`

Emitted when a column's title is clicked with either
`@GlobalScope.MOUSE_BUTTON_LEFT<class_@GlobalScope_constant_MOUSE_BUTTON_LEFT>`
or
`@GlobalScope.MOUSE_BUTTON_RIGHT<class_@GlobalScope_constant_MOUSE_BUTTON_RIGHT>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**custom\_item\_clicked**(mouse\_button\_index: `int<class_int>`)
`🔗<class_Tree_signal_custom_item_clicked>`

Emitted when an item with
`TreeItem.CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>` is
clicked with a mouse button.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**custom\_popup\_edited**(arrow\_clicked: `bool<class_bool>`)
`🔗<class_Tree_signal_custom_popup_edited>`

Emitted when a cell with the
`TreeItem.CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>` is
clicked to be edited.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**empty\_clicked**(click\_position: `Vector2<class_Vector2>`,
mouse\_button\_index: `int<class_int>`)
`🔗<class_Tree_signal_empty_clicked>`

Emitted when a mouse button is clicked in the empty space of the tree.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_activated**() `🔗<class_Tree_signal_item_activated>`

Emitted when an item is double-clicked, or selected with a `ui_accept`
input event (e.g. using `Enter` or `Space` on the keyboard).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_collapsed**(item: `TreeItem<class_TreeItem>`)
`🔗<class_Tree_signal_item_collapsed>`

Emitted when an item is collapsed by a click on the folding arrow.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_edited**() `🔗<class_Tree_signal_item_edited>`

Emitted when an item is edited.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_icon\_double\_clicked**()
`🔗<class_Tree_signal_item_icon_double_clicked>`

Emitted when an item's icon is double-clicked. For a signal that emits
when any part of the item is double-clicked, see
`item_activated<class_Tree_signal_item_activated>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_mouse\_selected**(mouse\_position: `Vector2<class_Vector2>`,
mouse\_button\_index: `int<class_int>`)
`🔗<class_Tree_signal_item_mouse_selected>`

Emitted when an item is selected with a mouse button.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_selected**() `🔗<class_Tree_signal_item_selected>`

Emitted when an item is selected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**multi\_selected**(item: `TreeItem<class_TreeItem>`, column:
`int<class_int>`, selected: `bool<class_bool>`)
`🔗<class_Tree_signal_multi_selected>`

Emitted instead of `item_selected<class_Tree_signal_item_selected>` if
`select_mode<class_Tree_property_select_mode>` is set to
`SELECT_MULTI<class_Tree_constant_SELECT_MULTI>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**nothing\_selected**() `🔗<class_Tree_signal_nothing_selected>`

Emitted when a left mouse button click does not select any item.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SelectMode**: `🔗<enum_Tree_SelectMode>`

classref-enumeration-constant

`SelectMode<enum_Tree_SelectMode>` **SELECT\_SINGLE** = `0`

Allows selection of a single cell at a time. From the perspective of
items, only a single item is allowed to be selected. And there is only
one column selected in the selected item.

The focus cursor is always hidden in this mode, but it is positioned at
the current selection, making the currently selected item the currently
focused item.

classref-enumeration-constant

`SelectMode<enum_Tree_SelectMode>` **SELECT\_ROW** = `1`

Allows selection of a single row at a time. From the perspective of
items, only a single items is allowed to be selected. And all the
columns are selected in the selected item.

The focus cursor is always hidden in this mode, but it is positioned at
the first column of the current selection, making the currently selected
item the currently focused item.

classref-enumeration-constant

`SelectMode<enum_Tree_SelectMode>` **SELECT\_MULTI** = `2`

Allows selection of multiple cells at the same time. From the
perspective of items, multiple items are allowed to be selected. And
there can be multiple columns selected in each selected item.

The focus cursor is visible in this mode, the item or column under the
cursor is not necessarily selected.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DropModeFlags**: `🔗<enum_Tree_DropModeFlags>`

classref-enumeration-constant

`DropModeFlags<enum_Tree_DropModeFlags>` **DROP\_MODE\_DISABLED** = `0`

Disables all drop sections, but still allows to detect the "on item"
drop section by
`get_drop_section_at_position<class_Tree_method_get_drop_section_at_position>`.

\*\*Note:\*\* This is the default flag, it has no effect when combined
with other flags.

classref-enumeration-constant

`DropModeFlags<enum_Tree_DropModeFlags>` **DROP\_MODE\_ON\_ITEM** = `1`

Enables the "on item" drop section. This drop section covers the entire
item.

When combined with
`DROP_MODE_INBETWEEN<class_Tree_constant_DROP_MODE_INBETWEEN>`, this
drop section halves the height and stays centered vertically.

classref-enumeration-constant

`DropModeFlags<enum_Tree_DropModeFlags>` **DROP\_MODE\_INBETWEEN** = `2`

Enables "above item" and "below item" drop sections. The "above item"
drop section covers the top half of the item, and the "below item" drop
section covers the bottom half.

When combined with
`DROP_MODE_ON_ITEM<class_Tree_constant_DROP_MODE_ON_ITEM>`, these drop
sections halves the height and stays on top / bottom accordingly.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_reselect** = `false`
`🔗<class_Tree_property_allow_reselect>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_reselect**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_allow\_reselect**()

If `true`, the currently selected cell may be selected again.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **allow\_rmb\_select** = `false`
`🔗<class_Tree_property_allow_rmb_select>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_rmb\_select**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_allow\_rmb\_select**()

If `true`, a right mouse button click can select items.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **allow\_search** = `true`
`🔗<class_Tree_property_allow_search>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_search**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_allow\_search**()

If `true`, allows navigating the **Tree** with letter keys through
incremental search.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **column\_titles\_visible** = `false`
`🔗<class_Tree_property_column_titles_visible>`

classref-property-setget

-   `void (No return value.)` **set\_column\_titles\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **are\_column\_titles\_visible**()

If `true`, column titles are visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **columns** = `1` `🔗<class_Tree_property_columns>`

classref-property-setget

-   `void (No return value.)` **set\_columns**(value: `int<class_int>`)
-   `int<class_int>` **get\_columns**()

The number of columns.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **drop\_mode\_flags** = `0`
`🔗<class_Tree_property_drop_mode_flags>`

classref-property-setget

-   `void (No return value.)` **set\_drop\_mode\_flags**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_drop\_mode\_flags**()

The drop mode as an OR combination of flags. See
`DropModeFlags<enum_Tree_DropModeFlags>` constants. Once dropping is
done, reverts to
`DROP_MODE_DISABLED<class_Tree_constant_DROP_MODE_DISABLED>`. Setting
this during
`Control._can_drop_data<class_Control_private_method__can_drop_data>` is
recommended.

This controls the drop sections, i.e. the decision and drawing of
possible drop locations based on the mouse position.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_recursive\_folding** = `true`
`🔗<class_Tree_property_enable_recursive_folding>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_recursive\_folding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_recursive\_folding\_enabled**()

If `true`, recursive folding is enabled for this **Tree**. Holding down
`Shift` while clicking the fold arrow or using `ui_right`/`ui_left`
shortcuts collapses or uncollapses the `TreeItem<class_TreeItem>` and
all its descendants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hide\_folding** = `false`
`🔗<class_Tree_property_hide_folding>`

classref-property-setget

-   `void (No return value.)` **set\_hide\_folding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_folding\_hidden**()

If `true`, the folding arrow is hidden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hide\_root** = `false`
`🔗<class_Tree_property_hide_root>`

classref-property-setget

-   `void (No return value.)` **set\_hide\_root**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_root\_hidden**()

If `true`, the tree's root is hidden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_horizontal\_enabled** = `true`
`🔗<class_Tree_property_scroll_horizontal_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_h\_scroll\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_h\_scroll\_enabled**()

If `true`, enables horizontal scrolling.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_vertical\_enabled** = `true`
`🔗<class_Tree_property_scroll_vertical_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_v\_scroll\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_v\_scroll\_enabled**()

If `true`, enables vertical scrolling.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SelectMode<enum_Tree_SelectMode>` **select\_mode** = `0`
`🔗<class_Tree_property_select_mode>`

classref-property-setget

-   `void (No return value.)` **set\_select\_mode**(value:
    `SelectMode<enum_Tree_SelectMode>`)
-   `SelectMode<enum_Tree_SelectMode>` **get\_select\_mode**()

Allows single or multiple selection. See the
`SelectMode<enum_Tree_SelectMode>` constants.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear**() `🔗<class_Tree_method_clear>`

Clears the tree. This removes all items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **create\_item**(parent:
`TreeItem<class_TreeItem>` = null, index: `int<class_int>` = -1)
`🔗<class_Tree_method_create_item>`

Creates an item in the tree and adds it as a child of `parent`, which
can be either a valid `TreeItem<class_TreeItem>` or `null`.

If `parent` is `null`, the root item will be the parent, or the new item
will be the root itself if the tree is empty.

The new item will be the `index`-th child of parent, or it will be the
last child if there are not enough siblings.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **deselect\_all**()
`🔗<class_Tree_method_deselect_all>`

Deselects all tree items (rows and columns). In
`SELECT_MULTI<class_Tree_constant_SELECT_MULTI>` mode also removes
selection cursor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **edit\_selected**(force\_edit: `bool<class_bool>` =
false) `🔗<class_Tree_method_edit_selected>`

Edits the selected tree item as if it was clicked.

Either the item must be set editable with
`TreeItem.set_editable<class_TreeItem_method_set_editable>` or
`force_edit` must be `true`.

Returns `true` if the item could be edited. Fails if no item is
selected.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **ensure\_cursor\_is\_visible**()
`🔗<class_Tree_method_ensure_cursor_is_visible>`

Makes the currently focused cell visible.

This will scroll the tree if necessary. In
`SELECT_ROW<class_Tree_constant_SELECT_ROW>` mode, this will not do
horizontal scrolling, as all the cells in the selected row is focused
logically.

\*\*Note:\*\* Despite the name of this method, the focus cursor itself
is only visible in `SELECT_MULTI<class_Tree_constant_SELECT_MULTI>`
mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_button\_id\_at\_position**(position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_button_id_at_position>`

Returns the button ID at `position`, or -1 if no button is there.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_column\_at\_position**(position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_at_position>`

Returns the column index at `position`, or -1 if no item is there.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_column\_expand\_ratio**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_expand_ratio>`

Returns the expand ratio assigned to the column.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_column\_title**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_title>`

Returns the column's title.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**get\_column\_title\_alignment**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_title_alignment>`

Returns the column title alignment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TextDirection<enum_Control_TextDirection>`
**get\_column\_title\_direction**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_title_direction>`

Returns column title base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_column\_title\_language**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_title_language>`

Returns column title language code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_column\_width**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_column_width>`

Returns the column's width in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_custom\_popup\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_custom_popup_rect>`

Returns the rectangle for custom popups. Helper to create custom cell
controls that display a popup. See
`TreeItem.set_cell_mode<class_TreeItem_method_set_cell_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_drop\_section\_at\_position**(position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_drop_section_at_position>`

Returns the drop section at `position`, or -100 if no item is there.

Values -1, 0, or 1 will be returned for the "above item", "on item", and
"below item" drop sections, respectively. See
`DropModeFlags<enum_Tree_DropModeFlags>` for a description of each drop
section.

To get the item which the returned drop section is relative to, use
`get_item_at_position<class_Tree_method_get_item_at_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_edited**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_edited>`

Returns the currently edited item. Can be used with
`item_edited<class_Tree_signal_item_edited>` to get the item that was
modified.

gdscript

func \_ready():  
$Tree.item\_edited.connect(on\_Tree\_item\_edited)

func on\_Tree\_item\_edited():  
print($Tree.get\_edited()) \# This item just got edited (e.g. checked).

csharp

public override void \_Ready() { GetNode&lt;Tree&gt;("Tree").ItemEdited
+= OnTreeItemEdited; }

public void OnTreeItemEdited() {
GD.Print(GetNode&lt;Tree&gt;("Tree").GetEdited()); // This item just got
edited (e.g. checked). }

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_edited\_column**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_edited_column>`

Returns the column for the currently edited item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_item\_area\_rect**(item:
`TreeItem<class_TreeItem>`, column: `int<class_int>` = -1,
button\_index: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_item_area_rect>`

Returns the rectangle area for the specified `TreeItem<class_TreeItem>`.
If `column` is specified, only get the position and size of that column,
otherwise get the rectangle containing all columns. If a button index is
specified, the rectangle of that button will be returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_item\_at\_position**(position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_item_at_position>`

Returns the tree item at the specified position (relative to the tree
origin position).

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_next\_selected**(from:
`TreeItem<class_TreeItem>`) `🔗<class_Tree_method_get_next_selected>`

Returns the next selected `TreeItem<class_TreeItem>` after the given
one, or `null` if the end is reached.

If `from` is `null`, this returns the first selected item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_pressed\_button**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_pressed_button>`

Returns the last pressed button's index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_root**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_root>`

Returns the tree's root item, or `null` if the tree is empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_scroll**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_scroll>`

Returns the current scrolling position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_selected**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_selected>`

Returns the currently focused item, or `null` if no item is focused.

In `SELECT_ROW<class_Tree_constant_SELECT_ROW>` and
`SELECT_SINGLE<class_Tree_constant_SELECT_SINGLE>` modes, the focused
item is same as the selected item. In
`SELECT_MULTI<class_Tree_constant_SELECT_MULTI>` mode, the focused item
is the item under the focus cursor, not necessarily selected.

To get the currently selected item(s), use
`get_next_selected<class_Tree_method_get_next_selected>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selected\_column**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_get_selected_column>`

Returns the currently focused column, or -1 if no column is focused.

In `SELECT_SINGLE<class_Tree_constant_SELECT_SINGLE>` mode, the focused
column is the selected column. In
`SELECT_ROW<class_Tree_constant_SELECT_ROW>` mode, the focused column is
always 0 if any item is selected. In
`SELECT_MULTI<class_Tree_constant_SELECT_MULTI>` mode, the focused
column is the column under the focus cursor, and there are not
necessarily any column selected.

To tell whether a column of an item is selected, use
`TreeItem.is_selected<class_TreeItem_method_is_selected>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_column\_clipping\_content**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_is_column_clipping_content>`

Returns `true` if the column has enabled clipping (see
`set_column_clip_content<class_Tree_method_set_column_clip_content>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_column\_expanding**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Tree_method_is_column_expanding>`

Returns `true` if the column has enabled expanding (see
`set_column_expand<class_Tree_method_set_column_expand>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scroll\_to\_item**(item:
`TreeItem<class_TreeItem>`, center\_on\_item: `bool<class_bool>` =
false) `🔗<class_Tree_method_scroll_to_item>`

Causes the **Tree** to jump to the specified `TreeItem<class_TreeItem>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_clip\_content**(column:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_Tree_method_set_column_clip_content>`

Allows to enable clipping for column's content, making the content size
ignored.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_column\_custom\_minimum\_width**(column: `int<class_int>`,
min\_width: `int<class_int>`)
`🔗<class_Tree_method_set_column_custom_minimum_width>`

Overrides the calculated minimum width of a column. It can be set to `0`
to restore the default behavior. Columns that have the "Expand" flag
will use their "min\_width" in a similar fashion to
`Control.size_flags_stretch_ratio<class_Control_property_size_flags_stretch_ratio>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_expand**(column:
`int<class_int>`, expand: `bool<class_bool>`)
`🔗<class_Tree_method_set_column_expand>`

If `true`, the column will have the "Expand" flag of
`Control<class_Control>`. Columns that have the "Expand" flag will use
their expand ratio in a similar fashion to
`Control.size_flags_stretch_ratio<class_Control_property_size_flags_stretch_ratio>`
(see
`set_column_expand_ratio<class_Tree_method_set_column_expand_ratio>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_expand\_ratio**(column:
`int<class_int>`, ratio: `int<class_int>`)
`🔗<class_Tree_method_set_column_expand_ratio>`

Sets the relative expand ratio for a column. See
`set_column_expand<class_Tree_method_set_column_expand>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_title**(column:
`int<class_int>`, title: `String<class_String>`)
`🔗<class_Tree_method_set_column_title>`

Sets the title of a column.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_title\_alignment**(column:
`int<class_int>`, title\_alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
`🔗<class_Tree_method_set_column_title_alignment>`

Sets the column title alignment. Note that
`@GlobalScope.HORIZONTAL_ALIGNMENT_FILL<class_@GlobalScope_constant_HORIZONTAL_ALIGNMENT_FILL>`
is not supported for column titles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_title\_direction**(column:
`int<class_int>`, direction:
`TextDirection<enum_Control_TextDirection>`)
`🔗<class_Tree_method_set_column_title_direction>`

Sets column title base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_column\_title\_language**(column:
`int<class_int>`, language: `String<class_String>`)
`🔗<class_Tree_method_set_column_title_language>`

Sets language code of column title used for line-breaking and text
shaping algorithms, if left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_selected**(item:
`TreeItem<class_TreeItem>`, column: `int<class_int>`)
`🔗<class_Tree_method_set_selected>`

Selects the specified `TreeItem<class_TreeItem>` and column.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **children\_hl\_line\_color** =
`Color(0.27, 0.27, 0.27, 1)`
`🔗<class_Tree_theme_color_children_hl_line_color>`

The `Color<class_Color>` of the relationship lines between the selected
`TreeItem<class_TreeItem>` and its children.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **custom\_button\_font\_highlight** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_Tree_theme_color_custom_button_font_highlight>`

Text `Color<class_Color>` for a
`TreeItem.CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>`
mode cell when it's hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **drop\_position\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Tree_theme_color_drop_position_color>`

`Color<class_Color>` used to draw possible drop locations. See
`DropModeFlags<enum_Tree_DropModeFlags>` constants for further
description of drop locations.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.7, 0.7, 0.7, 1)`
`🔗<class_Tree_theme_color_font_color>`

Default text `Color<class_Color>` of the item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_disabled\_color** =
`Color(0.875, 0.875, 0.875, 0.5)`
`🔗<class_Tree_theme_color_font_disabled_color>`

Text `Color<class_Color>` for a
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell when it's non-editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_Tree_theme_color_font_outline_color>`

The tint of text outline of the item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_selected\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Tree_theme_color_font_selected_color>`

Text `Color<class_Color>` used when the item is selected.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **guide\_color** = `Color(0.7, 0.7, 0.7, 0.25)`
`🔗<class_Tree_theme_color_guide_color>`

`Color<class_Color>` of the guideline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **parent\_hl\_line\_color** =
`Color(0.27, 0.27, 0.27, 1)`
`🔗<class_Tree_theme_color_parent_hl_line_color>`

The `Color<class_Color>` of the relationship lines between the selected
`TreeItem<class_TreeItem>` and its parents.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **relationship\_line\_color** =
`Color(0.27, 0.27, 0.27, 1)`
`🔗<class_Tree_theme_color_relationship_line_color>`

The default `Color<class_Color>` of the relationship lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **title\_button\_color** =
`Color(0.875, 0.875, 0.875, 1)`
`🔗<class_Tree_theme_color_title_button_color>`

Default text `Color<class_Color>` of the title button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **button\_margin** = `4`
`🔗<class_Tree_theme_constant_button_margin>`

The horizontal space between each button in a cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **children\_hl\_line\_width** = `1`
`🔗<class_Tree_theme_constant_children_hl_line_width>`

The width of the relationship lines between the selected
`TreeItem<class_TreeItem>` and its children.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **draw\_guides** = `1`
`🔗<class_Tree_theme_constant_draw_guides>`

Draws the guidelines if not zero, this acts as a boolean. The guideline
is a horizontal line drawn at the bottom of each item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **draw\_relationship\_lines** = `0`
`🔗<class_Tree_theme_constant_draw_relationship_lines>`

Draws the relationship lines if not zero, this acts as a boolean.
Relationship lines are drawn at the start of child items to show
hierarchy.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_Tree_theme_constant_h_separation>`

The horizontal space between item cells. This is also used as the margin
at the start of an item when folding is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **icon\_max\_width** = `0`
`🔗<class_Tree_theme_constant_icon_max_width>`

The maximum allowed width of the icon in item's cells. This limit is
applied on top of the default size of the icon, but before the value set
with
`TreeItem.set_icon_max_width<class_TreeItem_method_set_icon_max_width>`.
The height is adjusted according to the icon's ratio.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **inner\_item\_margin\_bottom** = `0`
`🔗<class_Tree_theme_constant_inner_item_margin_bottom>`

The inner bottom margin of a cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **inner\_item\_margin\_left** = `0`
`🔗<class_Tree_theme_constant_inner_item_margin_left>`

The inner left margin of a cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **inner\_item\_margin\_right** = `0`
`🔗<class_Tree_theme_constant_inner_item_margin_right>`

The inner right margin of a cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **inner\_item\_margin\_top** = `0`
`🔗<class_Tree_theme_constant_inner_item_margin_top>`

The inner top margin of a cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **item\_margin** = `16`
`🔗<class_Tree_theme_constant_item_margin>`

The horizontal margin at the start of an item. This is used when folding
is enabled for the item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_Tree_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_Tree_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **parent\_hl\_line\_margin** = `0`
`🔗<class_Tree_theme_constant_parent_hl_line_margin>`

The space between the parent relationship lines for the selected
`TreeItem<class_TreeItem>` and the relationship lines to its siblings
that are not selected.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **parent\_hl\_line\_width** = `1`
`🔗<class_Tree_theme_constant_parent_hl_line_width>`

The width of the relationship lines between the selected
`TreeItem<class_TreeItem>` and its parents.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **relationship\_line\_width** = `1`
`🔗<class_Tree_theme_constant_relationship_line_width>`

The default width of the relationship lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scroll\_border** = `4`
`🔗<class_Tree_theme_constant_scroll_border>`

The maximum distance between the mouse cursor and the control's border
to trigger border scrolling when dragging.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scroll\_speed** = `12`
`🔗<class_Tree_theme_constant_scroll_speed>`

The speed of border scrolling.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scrollbar\_h\_separation** = `4`
`🔗<class_Tree_theme_constant_scrollbar_h_separation>`

The horizontal separation of tree content and scrollbar.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scrollbar\_margin\_bottom** = `-1`
`🔗<class_Tree_theme_constant_scrollbar_margin_bottom>`

The bottom margin of the scrollbars. When negative, uses
`panel<class_Tree_theme_style_panel>` bottom margin.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scrollbar\_margin\_left** = `-1`
`🔗<class_Tree_theme_constant_scrollbar_margin_left>`

The left margin of the horizontal scrollbar. When negative, uses
`panel<class_Tree_theme_style_panel>` left margin.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scrollbar\_margin\_right** = `-1`
`🔗<class_Tree_theme_constant_scrollbar_margin_right>`

The right margin of the scrollbars. When negative, uses
`panel<class_Tree_theme_style_panel>` right margin.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scrollbar\_margin\_top** = `-1`
`🔗<class_Tree_theme_constant_scrollbar_margin_top>`

The top margin of the vertical scrollbar. When negative, uses
`panel<class_Tree_theme_style_panel>` top margin.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **scrollbar\_v\_separation** = `4`
`🔗<class_Tree_theme_constant_scrollbar_v_separation>`

The vertical separation of tree content and scrollbar.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **v\_separation** = `4`
`🔗<class_Tree_theme_constant_v_separation>`

The vertical padding inside each item, i.e. the distance between the
item's content and top/bottom border.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_Tree_theme_font_font>`

`Font<class_Font>` of the item's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **title\_button\_font**
`🔗<class_Tree_theme_font_title_button_font>`

`Font<class_Font>` of the title button's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_Tree_theme_font_size_font_size>`

Font size of the item's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **title\_button\_font\_size**
`🔗<class_Tree_theme_font_size_title_button_font_size>`

Font size of the title button's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **arrow** `🔗<class_Tree_theme_icon_arrow>`

The arrow icon used when a foldable item is not collapsed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **arrow\_collapsed**
`🔗<class_Tree_theme_icon_arrow_collapsed>`

The arrow icon used when a foldable item is collapsed (for left-to-right
layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **arrow\_collapsed\_mirrored**
`🔗<class_Tree_theme_icon_arrow_collapsed_mirrored>`

The arrow icon used when a foldable item is collapsed (for right-to-left
layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **checked**
`🔗<class_Tree_theme_icon_checked>`

The check icon to display when the
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell is checked and editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **checked\_disabled**
`🔗<class_Tree_theme_icon_checked_disabled>`

The check icon to display when the
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell is checked and non-editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **indeterminate**
`🔗<class_Tree_theme_icon_indeterminate>`

The check icon to display when the
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell is indeterminate and editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **indeterminate\_disabled**
`🔗<class_Tree_theme_icon_indeterminate_disabled>`

The check icon to display when the
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell is indeterminate and non-editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **select\_arrow**
`🔗<class_Tree_theme_icon_select_arrow>`

The arrow icon to display for the
`TreeItem.CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>` mode
cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **unchecked**
`🔗<class_Tree_theme_icon_unchecked>`

The check icon to display when the
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell is unchecked and editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **unchecked\_disabled**
`🔗<class_Tree_theme_icon_unchecked_disabled>`

The check icon to display when the
`TreeItem.CELL_MODE_CHECK<class_TreeItem_constant_CELL_MODE_CHECK>` mode
cell is unchecked and non-editable (see
`TreeItem.set_editable<class_TreeItem_method_set_editable>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **updown**
`🔗<class_Tree_theme_icon_updown>`

The updown arrow icon to display for the
`TreeItem.CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>` mode
cell.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **button\_pressed**
`🔗<class_Tree_theme_style_button_pressed>`

`StyleBox<class_StyleBox>` used when a button in the tree is pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **cursor**
`🔗<class_Tree_theme_style_cursor>`

`StyleBox<class_StyleBox>` used for the cursor, when the **Tree** is
being focused.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **cursor\_unfocused**
`🔗<class_Tree_theme_style_cursor_unfocused>`

`StyleBox<class_StyleBox>` used for the cursor, when the **Tree** is not
being focused.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **custom\_button**
`🔗<class_Tree_theme_style_custom_button>`

Default `StyleBox<class_StyleBox>` for a
`TreeItem.CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>`
mode cell when button is enabled with
`TreeItem.set_custom_as_button<class_TreeItem_method_set_custom_as_button>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **custom\_button\_hover**
`🔗<class_Tree_theme_style_custom_button_hover>`

`StyleBox<class_StyleBox>` for a
`TreeItem.CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>`
mode button cell when it's hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **custom\_button\_pressed**
`🔗<class_Tree_theme_style_custom_button_pressed>`

`StyleBox<class_StyleBox>` for a
`TreeItem.CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>`
mode button cell when it's pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **focus** `🔗<class_Tree_theme_style_focus>`

The focused style for the **Tree**, drawn on top of everything.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **panel** `🔗<class_Tree_theme_style_panel>`

The background style for the **Tree**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **selected**
`🔗<class_Tree_theme_style_selected>`

`StyleBox<class_StyleBox>` for the selected items, used when the
**Tree** is not being focused.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **selected\_focus**
`🔗<class_Tree_theme_style_selected_focus>`

`StyleBox<class_StyleBox>` for the selected items, used when the
**Tree** is being focused.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **title\_button\_hover**
`🔗<class_Tree_theme_style_title_button_hover>`

`StyleBox<class_StyleBox>` used when the title button is being hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **title\_button\_normal**
`🔗<class_Tree_theme_style_title_button_normal>`

Default `StyleBox<class_StyleBox>` for the title button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **title\_button\_pressed**
`🔗<class_Tree_theme_style_title_button_pressed>`

`StyleBox<class_StyleBox>` used when the title button is being pressed.
