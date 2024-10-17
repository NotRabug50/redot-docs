github\_url  
hide

# @GDScript

Built-in GDScript constants, functions, and annotations.

classref-introduction-group

## Description

A list of GDScript-specific utility functions and annotations accessible
from any script.

For the list of the global functions and constants see
`@GlobalScope<class_@GlobalScope>`.

classref-introduction-group

## Tutorials

-   `GDScript exports <../tutorials/scripting/gdscript/gdscript_exports>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**PI** = `3.14159265358979` `🔗<class_@GDScript_constant_PI>`

Constant that represents how many times the diameter of a circle fits
around its perimeter. This is equivalent to `TAU / 2`, or 180 degrees in
rotations.

classref-constant

**TAU** = `6.28318530717959` `🔗<class_@GDScript_constant_TAU>`

The circle constant, the circumference of the unit circle in radians.
This is equivalent to `PI * 2`, or 360 degrees in rotations.

classref-constant

**INF** = `inf` `🔗<class_@GDScript_constant_INF>`

Positive floating-point infinity. This is the result of floating-point
division when the divisor is `0.0`. For negative infinity, use `-INF`.
Dividing by `-0.0` will result in negative infinity if the numerator is
positive, so dividing by `0.0` is not the same as dividing by `-0.0`
(despite `0.0 == -0.0` returning `true`).

\*\*Warning:\*\* Numeric infinity is only a concept with floating-point
numbers, and has no equivalent for integers. Dividing an integer number
by `0` will not result in `INF<class_@GDScript_constant_INF>` and will
result in a run-time error instead.

classref-constant

**NAN** = `nan` `🔗<class_@GDScript_constant_NAN>`

"Not a Number", an invalid floating-point value.
`NAN<class_@GDScript_constant_NAN>` has special properties, including
that `!=` always returns `true`, while other comparison operators always
return `false`. This is true even when comparing with itself
(`NAN == NAN` returns `false` and `NAN != NAN` returns `true`). It is
returned by some invalid operations, such as dividing floating-point
`0.0` by `0.0`.

\*\*Warning:\*\* "Not a Number" is only a concept with floating-point
numbers, and has no equivalent for integers. Dividing an integer `0` by
`0` will not result in `NAN<class_@GDScript_constant_NAN>` and will
result in a run-time error instead.

classref-section-separator

------------------------------------------------------------------------

## Annotations

classref-annotation

**@export**() `🔗<class_@GDScript_annotation_@export>`

Mark the following property as exported (editable in the Inspector dock
and saved to disk). To control the type of the exported property, use
the type hint notation.

    extends Node

    enum Direction {LEFT, RIGHT, UP, DOWN}

    # Built-in types.
    @export var string = ""
    @export var int_number = 5
    @export var float_number: float = 5

    # Enums.
    @export var type: Variant.Type
    @export var format: Image.Format
    @export var direction: Direction

    # Resources.
    @export var image: Image
    @export var custom_resource: CustomResource

    # Nodes.
    @export var node: Node
    @export var custom_node: CustomNode

    # Typed arrays.
    @export var int_array: Array[int]
    @export var direction_array: Array[Direction]
    @export var image_array: Array[Image]
    @export var node_array: Array[Node]

\*\*Note:\*\* Custom resources and nodes should be registered as global
classes using `class_name`, since the Inspector currently only supports
global classes. Otherwise, a less specific type will be exported
instead.

\*\*Note:\*\* Node export is only supported in
`Node<class_Node>`-derived classes and has a number of other
limitations.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_category**(name: `String<class_String>`)
`🔗<class_@GDScript_annotation_@export_category>`

Define a new category for the following exported properties. This helps
to organize properties in the Inspector dock.

See also
`@GlobalScope.PROPERTY_USAGE_CATEGORY<class_@GlobalScope_constant_PROPERTY_USAGE_CATEGORY>`.

    @export_category("Statistics")
    @export var hp = 30
    @export var speed = 1.25

\*\*Note:\*\* Categories in the Inspector dock's list usually divide
properties coming from different classes (Node, Node2D, Sprite, etc.).
For better clarity, it's recommended to use
`@export_group<class_@GDScript_annotation_@export_group>` and
`@export_subgroup<class_@GDScript_annotation_@export_subgroup>`,
instead.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_color\_no\_alpha**()
`🔗<class_@GDScript_annotation_@export_color_no_alpha>`

Export a `Color<class_Color>`,
`Array<class_Array>`\[`Color<class_Color>`\], or
`PackedColorArray<class_PackedColorArray>` property without allowing its
transparency (`Color.a<class_Color_property_a>`) to be edited.

See also
`@GlobalScope.PROPERTY_HINT_COLOR_NO_ALPHA<class_@GlobalScope_constant_PROPERTY_HINT_COLOR_NO_ALPHA>`.

    @export_color_no_alpha var dye_color: Color
    @export_color_no_alpha var dye_colors: Array[Color]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_custom**(hint:
`PropertyHint<enum_@GlobalScope_PropertyHint>`, hint\_string:
`String<class_String>`, usage:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`PropertyUsageFlags<enum_@GlobalScope_PropertyUsageFlags>`\]
= 6) `🔗<class_@GDScript_annotation_@export_custom>`

Allows you to set a custom hint, hint string, and usage flags for the
exported property. Note that there's no validation done in GDScript, it
will just pass the parameters to the editor.

    @export_custom(PROPERTY_HINT_NONE, "suffix:m") var suffix: Vector3

\*\*Note:\*\* Regardless of the `usage` value, the
`@GlobalScope.PROPERTY_USAGE_SCRIPT_VARIABLE<class_@GlobalScope_constant_PROPERTY_USAGE_SCRIPT_VARIABLE>`
flag is always added, as with any explicitly declared script variable.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_dir**() `🔗<class_@GDScript_annotation_@export_dir>`

Export a `String<class_String>`,
`Array<class_Array>`\[`String<class_String>`\], or
`PackedStringArray<class_PackedStringArray>` property as a path to a
directory. The path will be limited to the project folder and its
subfolders. See
`@export_global_dir<class_@GDScript_annotation_@export_global_dir>` to
allow picking from the entire filesystem.

See also
`@GlobalScope.PROPERTY_HINT_DIR<class_@GlobalScope_constant_PROPERTY_HINT_DIR>`.

    @export_dir var sprite_folder_path: String
    @export_dir var sprite_folder_paths: Array[String]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_enum**(names: `String<class_String>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_enum>`

Export an `int<class_int>`, `String<class_String>`,
`Array<class_Array>`\[`int<class_int>`\],
`Array<class_Array>`\[`String<class_String>`\],
`PackedByteArray<class_PackedByteArray>`,
`PackedInt32Array<class_PackedInt32Array>`,
`PackedInt64Array<class_PackedInt64Array>`, or
`PackedStringArray<class_PackedStringArray>` property as an enumerated
list of options (or an array of options). If the property is an
`int<class_int>`, then the index of the value is stored, in the same
order the values are provided. You can add explicit values using a
colon. If the property is a `String<class_String>`, then the value is
stored.

See also
`@GlobalScope.PROPERTY_HINT_ENUM<class_@GlobalScope_constant_PROPERTY_HINT_ENUM>`.

    @export_enum("Warrior", "Magician", "Thief") var character_class: int
    @export_enum("Slow:30", "Average:60", "Very Fast:200") var character_speed: int
    @export_enum("Rebecca", "Mary", "Leah") var character_name: String

    @export_enum("Sword", "Spear", "Mace") var character_items: Array[int]
    @export_enum("double_jump", "climb", "dash") var character_skills: Array[String]

If you want to set an initial value, you must specify it explicitly:

    @export_enum("Rebecca", "Mary", "Leah") var character_name: String = "Rebecca"

If you want to use named GDScript enums, then use
`@export<class_@GDScript_annotation_@export>` instead:

    enum CharacterName {REBECCA, MARY, LEAH}
    @export var character_name: CharacterName

    enum CharacterItem {SWORD, SPEAR, MACE}
    @export var character_items: Array[CharacterItem]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_exp\_easing**(hints: `String<class_String>` = "", ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_exp_easing>`

Export a floating-point property with an easing editor widget.
Additional hints can be provided to adjust the behavior of the widget.
`"attenuation"` flips the curve, which makes it more intuitive for
editing attenuation properties. `"positive_only"` limits values to only
be greater than or equal to zero.

See also
`@GlobalScope.PROPERTY_HINT_EXP_EASING<class_@GlobalScope_constant_PROPERTY_HINT_EXP_EASING>`.

    @export_exp_easing var transition_speed
    @export_exp_easing("attenuation") var fading_attenuation
    @export_exp_easing("positive_only") var effect_power
    @export_exp_easing var speeds: Array[float]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_file**(filter: `String<class_String>` = "", ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_file>`

Export a `String<class_String>`,
`Array<class_Array>`\[`String<class_String>`\], or
`PackedStringArray<class_PackedStringArray>` property as a path to a
file. The path will be limited to the project folder and its subfolders.
See
`@export_global_file<class_@GDScript_annotation_@export_global_file>` to
allow picking from the entire filesystem.

If `filter` is provided, only matching files will be available for
picking.

See also
`@GlobalScope.PROPERTY_HINT_FILE<class_@GlobalScope_constant_PROPERTY_HINT_FILE>`.

    @export_file var sound_effect_path: String
    @export_file("*.txt") var notes_path: String
    @export_file var level_paths: Array[String]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags**(names: `String<class_String>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_flags>`

Export an integer property as a bit flag field. This allows to store
several "checked" or `true` values with one property, and comfortably
select them from the Inspector dock.

See also
`@GlobalScope.PROPERTY_HINT_FLAGS<class_@GlobalScope_constant_PROPERTY_HINT_FLAGS>`.

    @export_flags("Fire", "Water", "Earth", "Wind") var spell_elements = 0

You can add explicit values using a colon:

    @export_flags("Self:4", "Allies:8", "Foes:16") var spell_targets = 0

You can also combine several flags:

    @export_flags("Self:4", "Allies:8", "Self and Allies:12", "Foes:16")
    var spell_targets = 0

\*\*Note:\*\* A flag value must be at least `1` and at most
`2 ** 32 - 1`.

\*\*Note:\*\* Unlike
`@export_enum<class_@GDScript_annotation_@export_enum>`, the previous
explicit value is not taken into account. In the following example, A is
16, B is 2, C is 4.

    @export_flags("A:16", "B", "C") var x

You can also use the annotation on
`Array<class_Array>`\[`int<class_int>`\],
`PackedByteArray<class_PackedByteArray>`,
`PackedInt32Array<class_PackedInt32Array>`, and
`PackedInt64Array<class_PackedInt64Array>`

    @export_flags("Fire", "Water", "Earth", "Wind") var phase_elements: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_2d\_navigation**()
`🔗<class_@GDScript_annotation_@export_flags_2d_navigation>`

Export an integer property as a bit flag field for 2D navigation layers.
The widget in the Inspector dock will use the layer names defined in
`ProjectSettings.layer_names/2d_navigation/layer_1<class_ProjectSettings_property_layer_names/2d_navigation/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_2D_NAVIGATION<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_2D_NAVIGATION>`.

    @export_flags_2d_navigation var navigation_layers: int
    @export_flags_2d_navigation var navigation_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_2d\_physics**()
`🔗<class_@GDScript_annotation_@export_flags_2d_physics>`

Export an integer property as a bit flag field for 2D physics layers.
The widget in the Inspector dock will use the layer names defined in
`ProjectSettings.layer_names/2d_physics/layer_1<class_ProjectSettings_property_layer_names/2d_physics/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_2D_PHYSICS<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_2D_PHYSICS>`.

    @export_flags_2d_physics var physics_layers: int
    @export_flags_2d_physics var physics_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_2d\_render**()
`🔗<class_@GDScript_annotation_@export_flags_2d_render>`

Export an integer property as a bit flag field for 2D render layers. The
widget in the Inspector dock will use the layer names defined in
`ProjectSettings.layer_names/2d_render/layer_1<class_ProjectSettings_property_layer_names/2d_render/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_2D_RENDER<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_2D_RENDER>`.

    @export_flags_2d_render var render_layers: int
    @export_flags_2d_render var render_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_3d\_navigation**()
`🔗<class_@GDScript_annotation_@export_flags_3d_navigation>`

Export an integer property as a bit flag field for 3D navigation layers.
The widget in the Inspector dock will use the layer names defined in
`ProjectSettings.layer_names/3d_navigation/layer_1<class_ProjectSettings_property_layer_names/3d_navigation/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_3D_NAVIGATION<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_3D_NAVIGATION>`.

    @export_flags_3d_navigation var navigation_layers: int
    @export_flags_3d_navigation var navigation_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_3d\_physics**()
`🔗<class_@GDScript_annotation_@export_flags_3d_physics>`

Export an integer property as a bit flag field for 3D physics layers.
The widget in the Inspector dock will use the layer names defined in
`ProjectSettings.layer_names/3d_physics/layer_1<class_ProjectSettings_property_layer_names/3d_physics/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_3D_PHYSICS<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_3D_PHYSICS>`.

    @export_flags_3d_physics var physics_layers: int
    @export_flags_3d_physics var physics_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_3d\_render**()
`🔗<class_@GDScript_annotation_@export_flags_3d_render>`

Export an integer property as a bit flag field for 3D render layers. The
widget in the Inspector dock will use the layer names defined in
`ProjectSettings.layer_names/3d_render/layer_1<class_ProjectSettings_property_layer_names/3d_render/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_3D_RENDER<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_3D_RENDER>`.

    @export_flags_3d_render var render_layers: int
    @export_flags_3d_render var render_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_flags\_avoidance**()
`🔗<class_@GDScript_annotation_@export_flags_avoidance>`

Export an integer property as a bit flag field for navigation avoidance
layers. The widget in the Inspector dock will use the layer names
defined in
`ProjectSettings.layer_names/avoidance/layer_1<class_ProjectSettings_property_layer_names/avoidance/layer_1>`.

See also
`@GlobalScope.PROPERTY_HINT_LAYERS_AVOIDANCE<class_@GlobalScope_constant_PROPERTY_HINT_LAYERS_AVOIDANCE>`.

    @export_flags_avoidance var avoidance_layers: int
    @export_flags_avoidance var avoidance_layers_array: Array[int]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_global\_dir**()
`🔗<class_@GDScript_annotation_@export_global_dir>`

Export a `String<class_String>`,
`Array<class_Array>`\[`String<class_String>`\], or
`PackedStringArray<class_PackedStringArray>` property as an absolute
path to a directory. The path can be picked from the entire filesystem.
See `@export_dir<class_@GDScript_annotation_@export_dir>` to limit it to
the project folder and its subfolders.

See also
`@GlobalScope.PROPERTY_HINT_GLOBAL_DIR<class_@GlobalScope_constant_PROPERTY_HINT_GLOBAL_DIR>`.

    @export_global_dir var sprite_folder_path: String
    @export_global_dir var sprite_folder_paths: Array[String]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_global\_file**(filter: `String<class_String>` = "", ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_global_file>`

Export a `String<class_String>`,
`Array<class_Array>`\[`String<class_String>`\], or
`PackedStringArray<class_PackedStringArray>` property as an absolute
path to a file. The path can be picked from the entire filesystem. See
`@export_file<class_@GDScript_annotation_@export_file>` to limit it to
the project folder and its subfolders.

If `filter` is provided, only matching files will be available for
picking.

See also
`@GlobalScope.PROPERTY_HINT_GLOBAL_FILE<class_@GlobalScope_constant_PROPERTY_HINT_GLOBAL_FILE>`.

    @export_global_file var sound_effect_path: String
    @export_global_file("*.txt") var notes_path: String
    @export_global_file var multiple_paths: Array[String]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_group**(name: `String<class_String>`, prefix:
`String<class_String>` = "")
`🔗<class_@GDScript_annotation_@export_group>`

Define a new group for the following exported properties. This helps to
organize properties in the Inspector dock. Groups can be added with an
optional `prefix`, which would make group to only consider properties
that have this prefix. The grouping will break on the first property
that doesn't have a prefix. The prefix is also removed from the
property's name in the Inspector dock.

If no `prefix` is provided, then every following property will be added
to the group. The group ends when then next group or category is
defined. You can also force end a group by using this annotation with
empty strings for parameters, `@export_group("", "")`.

Groups cannot be nested, use
`@export_subgroup<class_@GDScript_annotation_@export_subgroup>` to add
subgroups within groups.

See also
`@GlobalScope.PROPERTY_USAGE_GROUP<class_@GlobalScope_constant_PROPERTY_USAGE_GROUP>`.

    @export_group("Racer Properties")
    @export var nickname = "Nick"
    @export var age = 26

    @export_group("Car Properties", "car_")
    @export var car_label = "Speedy"
    @export var car_number = 3

    @export_group("", "")
    @export var ungrouped_number = 3

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_multiline**()
`🔗<class_@GDScript_annotation_@export_multiline>`

Export a `String<class_String>`,
`Array<class_Array>`\[`String<class_String>`\],
`PackedStringArray<class_PackedStringArray>`,
`Dictionary<class_Dictionary>` or
`Array<class_Array>`\[`Dictionary<class_Dictionary>`\] property with a
large `TextEdit<class_TextEdit>` widget instead of a
`LineEdit<class_LineEdit>`. This adds support for multiline content and
makes it easier to edit large amount of text stored in the property.

See also
`@GlobalScope.PROPERTY_HINT_MULTILINE_TEXT<class_@GlobalScope_constant_PROPERTY_HINT_MULTILINE_TEXT>`.

    @export_multiline var character_biography
    @export_multiline var npc_dialogs: Array[String]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_node\_path**(type: `String<class_String>` = "", ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_node_path>`

Export a `NodePath<class_NodePath>` or
`Array<class_Array>`\[`NodePath<class_NodePath>`\] property with a
filter for allowed node types.

See also
`@GlobalScope.PROPERTY_HINT_NODE_PATH_VALID_TYPES<class_@GlobalScope_constant_PROPERTY_HINT_NODE_PATH_VALID_TYPES>`.

    @export_node_path("Button", "TouchScreenButton") var some_button
    @export_node_path("Button", "TouchScreenButton") var many_buttons: Array[NodePath]

\*\*Note:\*\* The type must be a native class or a globally registered
script (using the `class_name` keyword) that inherits
`Node<class_Node>`.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_placeholder**(placeholder: `String<class_String>`)
`🔗<class_@GDScript_annotation_@export_placeholder>`

Export a `String<class_String>`,
`Array<class_Array>`\[`String<class_String>`\], or
`PackedStringArray<class_PackedStringArray>` property with a placeholder
text displayed in the editor widget when no value is present.

See also
`@GlobalScope.PROPERTY_HINT_PLACEHOLDER_TEXT<class_@GlobalScope_constant_PROPERTY_HINT_PLACEHOLDER_TEXT>`.

    @export_placeholder("Name in lowercase") var character_id: String
    @export_placeholder("Name in lowercase") var friend_ids: Array[String]

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_range**(min: `float<class_float>`, max: `float<class_float>`,
step: `float<class_float>` = 1.0, extra\_hints: `String<class_String>` =
"", ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@export_range>`

Export an `int<class_int>`, `float<class_float>`,
`Array<class_Array>`\[`int<class_int>`\],
`Array<class_Array>`\[`float<class_float>`\],
`PackedByteArray<class_PackedByteArray>`,
`PackedInt32Array<class_PackedInt32Array>`,
`PackedInt64Array<class_PackedInt64Array>`,
`PackedFloat32Array<class_PackedFloat32Array>`, or
`PackedFloat64Array<class_PackedFloat64Array>` property as a range
value. The range must be defined by `min` and `max`, as well as an
optional `step` and a variety of extra hints. The `step` defaults to `1`
for integer properties. For floating-point numbers this value depends on
your
`EditorSettings.interface/inspector/default_float_step<class_EditorSettings_property_interface/inspector/default_float_step>`
setting.

If hints `"or_greater"` and `"or_less"` are provided, the editor widget
will not cap the value at range boundaries. The `"exp"` hint will make
the edited values on range to change exponentially. The `"hide_slider"`
hint will hide the slider element of the editor widget.

Hints also allow to indicate the units for the edited value. Using
`"radians_as_degrees"` you can specify that the actual value is in
radians, but should be displayed in degrees in the Inspector dock (the
range values are also in degrees). `"degrees"` allows to add a degree
sign as a unit suffix (the value is unchanged). Finally, a custom suffix
can be provided using `"suffix:unit"`, where "unit" can be any string.

See also
`@GlobalScope.PROPERTY_HINT_RANGE<class_@GlobalScope_constant_PROPERTY_HINT_RANGE>`.

    @export_range(0, 20) var number
    @export_range(-10, 20) var number
    @export_range(-10, 20, 0.2) var number: float
    @export_range(0, 20) var numbers: Array[float]

    @export_range(0, 100, 1, "or_greater") var power_percent
    @export_range(0, 100, 1, "or_greater", "or_less") var health_delta

    @export_range(-180, 180, 0.001, "radians_as_degrees") var angle_radians
    @export_range(0, 360, 1, "degrees") var angle_degrees
    @export_range(-8, 8, 2, "suffix:px") var target_offset

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_storage**() `🔗<class_@GDScript_annotation_@export_storage>`

Export a property with
`@GlobalScope.PROPERTY_USAGE_STORAGE<class_@GlobalScope_constant_PROPERTY_USAGE_STORAGE>`
flag. The property is not displayed in the editor, but it is serialized
and stored in the scene or resource file. This can be useful for
`@tool<class_@GDScript_annotation_@tool>` scripts. Also the property
value is copied when
`Resource.duplicate<class_Resource_method_duplicate>` or
`Node.duplicate<class_Node_method_duplicate>` is called, unlike
non-exported variables.

    var a # Not stored in the file, not displayed in the editor.
    @export_storage var b # Stored in the file, not displayed in the editor.
    @export var c: int # Stored in the file, displayed in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_subgroup**(name: `String<class_String>`, prefix:
`String<class_String>` = "")
`🔗<class_@GDScript_annotation_@export_subgroup>`

Define a new subgroup for the following exported properties. This helps
to organize properties in the Inspector dock. Subgroups work exactly
like groups, except they need a parent group to exist. See
`@export_group<class_@GDScript_annotation_@export_group>`.

See also
`@GlobalScope.PROPERTY_USAGE_SUBGROUP<class_@GlobalScope_constant_PROPERTY_USAGE_SUBGROUP>`.

    @export_group("Racer Properties")
    @export var nickname = "Nick"
    @export var age = 26

    @export_subgroup("Car Properties", "car_")
    @export var car_label = "Speedy"
    @export var car_number = 3

\*\*Note:\*\* Subgroups cannot be nested, they only provide one extra
level of depth. Just like the next group ends the previous group, so do
the subsequent subgroups.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@export\_tool\_button**(text: `String<class_String>`, icon:
`String<class_String>` = "")
`🔗<class_@GDScript_annotation_@export_tool_button>`

Export a `Callable<class_Callable>` property as a clickable button with
the label `text`. When the button is pressed, the callable is called.

If `icon` is specified, it is used to fetch an icon for the button via
`Control.get_theme_icon<class_Control_method_get_theme_icon>`, from the
`"EditorIcons"` theme type. If `icon` is omitted, the default
`"Callable"` icon is used instead.

Consider using the `EditorUndoRedoManager<class_EditorUndoRedoManager>`
to allow the action to be reverted safely.

See also
`@GlobalScope.PROPERTY_HINT_TOOL_BUTTON<class_@GlobalScope_constant_PROPERTY_HINT_TOOL_BUTTON>`.

    @tool
    extends Sprite2D

    @export_tool_button("Hello") var hello_action = hello
    @export_tool_button("Randomize the color!", "ColorRect")
    var randomize_color_action = randomize_color

    func hello():
        print("Hello world!")

    func randomize_color():
        var undo_redo = EditorInterface.get_editor_undo_redo()
        undo_redo.create_action("Randomized Sprite2D Color")
        undo_redo.add_do_property(self, &"self_modulate", Color(randf(), randf(), randf()))
        undo_redo.add_undo_property(self, &"self_modulate", self_modulate)
        undo_redo.commit_action()

\*\*Note:\*\* The property is exported without the
`@GlobalScope.PROPERTY_USAGE_STORAGE<class_@GlobalScope_constant_PROPERTY_USAGE_STORAGE>`
flag because a `Callable<class_Callable>` cannot be properly serialized
and stored in a file.

\*\*Note:\*\* In an exported project neither
`EditorInterface<class_EditorInterface>` nor
`EditorUndoRedoManager<class_EditorUndoRedoManager>` exist, which may
cause some scripts to break. To prevent this, you can use
`Engine.get_singleton<class_Engine_method_get_singleton>` and omit the
static type from the variable declaration:

    var undo_redo = Engine.get_singleton(&"EditorInterface").get_editor_undo_redo()

\*\*Note:\*\* Avoid storing lambda callables in member variables of
`RefCounted<class_RefCounted>`-based classes (e.g. resources), as this
can lead to memory leaks. Use only method callables and optionally
`Callable.bind<class_Callable_method_bind>` or
`Callable.unbind<class_Callable_method_unbind>`.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@icon**(icon\_path: `String<class_String>`)
`🔗<class_@GDScript_annotation_@icon>`

Add a custom icon to the current script. The icon specified at
`icon_path` is displayed in the Scene dock for every node of that class,
as well as in various editor dialogs.

    @icon("res://path/to/class/icon.svg")

\*\*Note:\*\* Only the script can have a custom icon. Inner classes are
not supported.

\*\*Note:\*\* As annotations describe their subject, the
`@icon<class_@GDScript_annotation_@icon>` annotation must be placed
before the class definition and inheritance.

\*\*Note:\*\* Unlike other annotations, the argument of the
`@icon<class_@GDScript_annotation_@icon>` annotation must be a string
literal (constant expressions are not supported).

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@onready**() `🔗<class_@GDScript_annotation_@onready>`

Mark the following property as assigned when the `Node<class_Node>` is
ready. Values for these properties are not assigned immediately when the
node is initialized (`Object._init<class_Object_private_method__init>`),
and instead are computed and stored right before
`Node._ready<class_Node_private_method__ready>`.

    @onready var character_name: Label = $Label

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@rpc**(mode: `String<class_String>` = "authority", sync:
`String<class_String>` = "call\_remote", transfer\_mode:
`String<class_String>` = "unreliable", transfer\_channel:
`int<class_int>` = 0) `🔗<class_@GDScript_annotation_@rpc>`

Mark the following method for remote procedure calls. See
`High-level multiplayer <../tutorials/networking/high_level_multiplayer>`.

If `mode` is set as `"any_peer"`, allows any peer to call this RPC
function. Otherwise, only the authority peer is allowed to call it and
`mode` should be kept as `"authority"`. When configuring functions as
RPCs with `Node.rpc_config<class_Node_method_rpc_config>`, each of these
modes respectively corresponds to the
`MultiplayerAPI.RPC_MODE_AUTHORITY<class_MultiplayerAPI_constant_RPC_MODE_AUTHORITY>`
and
`MultiplayerAPI.RPC_MODE_ANY_PEER<class_MultiplayerAPI_constant_RPC_MODE_ANY_PEER>`
RPC modes. See `RPCMode<enum_MultiplayerAPI_RPCMode>`. If a peer that is
not the authority tries to call a function that is only allowed for the
authority, the function will not be executed. If the error can be
detected locally (when the RPC configuration is consistent between the
local and the remote peer), an error message will be displayed on the
sender peer. Otherwise, the remote peer will detect the error and print
an error there.

If `sync` is set as `"call_remote"`, the function will only be executed
on the remote peer, but not locally. To run this function locally too,
set `sync` to `"call_local"`. When configuring functions as RPCs with
`Node.rpc_config<class_Node_method_rpc_config>`, this is equivalent to
setting `call_local` to `true`.

The `transfer_mode` accepted values are `"unreliable"`,
`"unreliable_ordered"`, or `"reliable"`. It sets the transfer mode of
the underlying `MultiplayerPeer<class_MultiplayerPeer>`. See
`MultiplayerPeer.transfer_mode<class_MultiplayerPeer_property_transfer_mode>`.

The `transfer_channel` defines the channel of the underlying
`MultiplayerPeer<class_MultiplayerPeer>`. See
`MultiplayerPeer.transfer_channel<class_MultiplayerPeer_property_transfer_channel>`.

The order of `mode`, `sync` and `transfer_mode` does not matter, but
values related to the same argument must not be used more than once.
`transfer_channel` always has to be the 4th argument (you must specify 3
preceding arguments).

    @rpc
    func fn(): pass

    @rpc("any_peer", "unreliable_ordered")
    func fn_update_pos(): pass

    @rpc("authority", "call_remote", "unreliable", 0) # Equivalent to @rpc
    func fn_default(): pass

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@static\_unload**() `🔗<class_@GDScript_annotation_@static_unload>`

Make a script with static variables to not persist after all references
are lost. If the script is loaded again the static variables will revert
to their default values.

\*\*Note:\*\* As annotations describe their subject, the
`@static_unload<class_@GDScript_annotation_@static_unload>` annotation
must be placed before the class definition and inheritance.

\*\*Warning:\*\* Currently, due to a bug, scripts are never freed, even
if `@static_unload<class_@GDScript_annotation_@static_unload>`
annotation is used.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@tool**() `🔗<class_@GDScript_annotation_@tool>`

Mark the current script as a tool script, allowing it to be loaded and
executed by the editor. See
`Running code in the editor <../tutorials/plugins/running_code_in_the_editor>`.

    @tool
    extends Node

\*\*Note:\*\* As annotations describe their subject, the
`@tool<class_@GDScript_annotation_@tool>` annotation must be placed
before the class definition and inheritance.

classref-item-separator

------------------------------------------------------------------------

classref-annotation

**@warning\_ignore**(warning: `String<class_String>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_annotation_@warning_ignore>`

Mark the following statement to ignore the specified `warning`. See
`GDScript warning system <../tutorials/scripting/gdscript/warning_system>`.

    func test():
        print("hello")
        return
        @warning_ignore("unreachable_code")
        print("unreachable")

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Color<class_Color>` **Color8**(r8: `int<class_int>`, g8:
`int<class_int>`, b8: `int<class_int>`, a8: `int<class_int>` = 255)
`🔗<class_@GDScript_method_Color8>`

Returns a `Color<class_Color>` constructed from red (`r8`), green
(`g8`), blue (`b8`), and optionally alpha (`a8`) integer channels, each
divided by `255.0` for their final value. Using
`Color8<class_@GDScript_method_Color8>` instead of the standard
`Color<class_Color>` constructor is useful when you need to match exact
color values in an `Image<class_Image>`.

    var red = Color8(255, 0, 0)             # Same as Color(1, 0, 0).
    var dark_blue = Color8(0, 0, 51)        # Same as Color(0, 0, 0.2).
    var my_color = Color8(306, 255, 0, 102) # Same as Color(1.2, 1, 0, 0.4).

\*\*Note:\*\* Due to the lower precision of
`Color8<class_@GDScript_method_Color8>` compared to the standard
`Color<class_Color>` constructor, a color created with
`Color8<class_@GDScript_method_Color8>` will generally not be equal to
the same color created with the standard `Color<class_Color>`
constructor. Use
`Color.is_equal_approx<class_Color_method_is_equal_approx>` for
comparisons to avoid issues with floating-point precision error.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **assert**(condition: `bool<class_bool>`,
message: `String<class_String>` = "")
`🔗<class_@GDScript_method_assert>`

Asserts that the `condition` is `true`. If the `condition` is `false`,
an error is generated. When running from the editor, the running project
will also be paused until you resume it. This can be used as a stronger
form of `@GlobalScope.push_error<class_@GlobalScope_method_push_error>`
for reporting errors to project developers or add-on users.

An optional `message` can be shown in addition to the generic "Assertion
failed" message. You can use this to provide additional details about
why the assertion failed.

\*\*Warning:\*\* For performance reasons, the code inside
`assert<class_@GDScript_method_assert>` is only executed in debug builds
or when running the project from the editor. Don't include code that has
side effects in an `assert<class_@GDScript_method_assert>` call.
Otherwise, the project will behave differently when exported in release
mode.

    # Imagine we always want speed to be between 0 and 20.
    var speed = -10
    assert(speed < 20) # True, the program will continue.
    assert(speed >= 0) # False, the program will stop.
    assert(speed >= 0 and speed < 20) # You can also combine the two conditional statements in one check.
    assert(speed < 20, "the speed limit is 20") # Show a message.

\*\*Note:\*\* `assert<class_@GDScript_method_assert>` is a keyword, not
a function. So you cannot access it as a `Callable<class_Callable>` or
use it inside expressions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **char**(char: `int<class_int>`)
`🔗<class_@GDScript_method_char>`

Returns a single character (as a `String<class_String>`) of the given
Unicode code point (which is compatible with ASCII code).

    var upper = char(65)      # upper is "A"
    var lower = char(65 + 32) # lower is "a"
    var euro = char(8364)     # euro is "€"

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **convert**(what: `Variant<class_Variant>`,
type: `int<class_int>`) `🔗<class_@GDScript_method_convert>`

**Deprecated:** Use
`@GlobalScope.type_convert<class_@GlobalScope_method_type_convert>`
instead.

Converts `what` to `type` in the best way possible. The `type` uses the
`Variant.Type<enum_@GlobalScope_Variant.Type>` values.

    var a = [4, 2.5, 1.2]
    print(a is Array) # Prints true

    var b = convert(a, TYPE_PACKED_BYTE_ARRAY)
    print(b)          # Prints [4, 2, 1]
    print(b is Array) # Prints false

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **dict\_to\_inst**(dictionary:
`Dictionary<class_Dictionary>`)
`🔗<class_@GDScript_method_dict_to_inst>`

Converts a `dictionary` (created with
`inst_to_dict<class_@GDScript_method_inst_to_dict>`) back to an Object
instance. Can be useful for deserializing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_stack**()
`🔗<class_@GDScript_method_get_stack>`

Returns an array of dictionaries representing the current call stack.
See also `print_stack<class_@GDScript_method_print_stack>`.

    func _ready():
        foo()

    func foo():
        bar()

    func bar():
        print(get_stack())

Starting from `_ready()`, `bar()` would print:

    [{function:bar, line:12, source:res://script.gd}, {function:foo, line:9, source:res://script.gd}, {function:_ready, line:6, source:res://script.gd}]

\*\*Note:\*\* This function only works if the running instance is
connected to a debugging server (i.e. an editor instance).
`get_stack<class_@GDScript_method_get_stack>` will not work in projects
exported in release mode, or in projects exported in debug mode if not
connected to a debugging server.

\*\*Note:\*\* Calling this function from a `Thread<class_Thread>` is not
supported. Doing so will return an empty array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **inst\_to\_dict**(instance:
`Object<class_Object>`) `🔗<class_@GDScript_method_inst_to_dict>`

Returns the passed `instance` converted to a Dictionary. Can be useful
for serializing.

\*\*Note:\*\* Cannot be used to serialize objects with built-in scripts
attached or objects allocated within built-in scripts.

    var foo = "bar"
    func _ready():
        var d = inst_to_dict(self)
        print(d.keys())
        print(d.values())

Prints out:

    [@subpath, @path, foo]
    [, res://test.gd, bar]

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_instance\_of**(value: `Variant<class_Variant>`,
type: `Variant<class_Variant>`)
`🔗<class_@GDScript_method_is_instance_of>`

Returns `true` if `value` is an instance of `type`. The `type` value
must be one of the following:

-   A constant from the `Variant.Type<enum_@GlobalScope_Variant.Type>`
    enumeration, for example
    `@GlobalScope.TYPE_INT<class_@GlobalScope_constant_TYPE_INT>`.
-   An `Object<class_Object>`-derived class which exists in
    `ClassDB<class_ClassDB>`, for example `Node<class_Node>`.
-   A `Script<class_Script>` (you can use any class, including inner
    one).

Unlike the right operand of the `is` operator, `type` can be a
non-constant value. The `is` operator supports more features (such as
typed arrays). Use the operator instead of this method if you do not
need dynamic type checking.

\*\*Examples:\*\*

    print(is_instance_of(a, TYPE_INT))
    print(is_instance_of(a, Node))
    print(is_instance_of(a, MyClass))
    print(is_instance_of(a, MyClass.InnerClass))

\*\*Note:\*\* If `value` and/or `type` are freed objects (see
`@GlobalScope.is_instance_valid<class_@GlobalScope_method_is_instance_valid>`),
or `type` is not one of the above options, this method will raise a
runtime error.

See also `@GlobalScope.typeof<class_@GlobalScope_method_typeof>`,
`type_exists<class_@GDScript_method_type_exists>`,
`Array.is_same_typed<class_Array_method_is_same_typed>` (and other
`Array<class_Array>` methods).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **len**(var: `Variant<class_Variant>`)
`🔗<class_@GDScript_method_len>`

Returns the length of the given Variant `var`. The length can be the
character count of a `String<class_String>` or
`StringName<class_StringName>`, the element count of any array type, or
the size of a `Dictionary<class_Dictionary>`. For every other Variant
type, a run-time error is generated and execution is stopped.

    var a = [1, 2, 3, 4]
    len(a) # Returns 4

    var b = "Hello!"
    len(b) # Returns 6

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>` **load**(path: `String<class_String>`)
`🔗<class_@GDScript_method_load>`

Returns a `Resource<class_Resource>` from the filesystem located at the
absolute `path`. Unless it's already referenced elsewhere (such as in
another script or in the scene), the resource is loaded from disk on
function call, which might cause a slight delay, especially when loading
large scenes. To avoid unnecessary delays when loading something
multiple times, either store the resource in a variable or use
`preload<class_@GDScript_method_preload>`. This method is equivalent of
using `ResourceLoader.load<class_ResourceLoader_method_load>` with
`ResourceLoader.CACHE_MODE_REUSE<class_ResourceLoader_constant_CACHE_MODE_REUSE>`.

\*\*Note:\*\* Resource paths can be obtained by right-clicking on a
resource in the FileSystem dock and choosing "Copy Path", or by dragging
the file from the FileSystem dock into the current script.

    # Load a scene called "main" located in the root of the project directory and cache it in a variable.
    var main = load("res://main.tscn") # main will contain a PackedScene resource.

\*\*Important:\*\* Relative paths are *not* relative to the script
calling this method, instead it is prefixed with `"res://"`. Loading
from relative paths might not work as expected.

This function is a simplified version of
`ResourceLoader.load<class_ResourceLoader_method_load>`, which can be
used for more advanced scenarios.

\*\*Note:\*\* Files have to be imported into the engine first to load
them using this function. If you want to load `Image<class_Image>`s at
run-time, you may use `Image.load<class_Image_method_load>`. If you want
to import audio files, you can use the snippet described in
`AudioStreamMP3.data<class_AudioStreamMP3_property_data>`.

\*\*Note:\*\* If
`ProjectSettings.editor/export/convert_text_resources_to_binary<class_ProjectSettings_property_editor/export/convert_text_resources_to_binary>`
is `true`, `load<class_@GDScript_method_load>` will not be able to read
converted files in an exported project. If you rely on run-time loading
of files present within the PCK, set
`ProjectSettings.editor/export/convert_text_resources_to_binary<class_ProjectSettings_property_editor/export/convert_text_resources_to_binary>`
to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>` **preload**(path: `String<class_String>`)
`🔗<class_@GDScript_method_preload>`

Returns a `Resource<class_Resource>` from the filesystem located at
`path`. During run-time, the resource is loaded when the script is being
parsed. This function effectively acts as a reference to that resource.
Note that this function requires `path` to be a constant
`String<class_String>`. If you want to load a resource from a
dynamic/variable path, use `load<class_@GDScript_method_load>`.

\*\*Note:\*\* Resource paths can be obtained by right-clicking on a
resource in the Assets Panel and choosing "Copy Path", or by dragging
the file from the FileSystem dock into the current script.

    # Create instance of a scene.
    var diamond = preload("res://diamond.tscn").instantiate()

\*\*Note:\*\* `preload<class_@GDScript_method_preload>` is a keyword,
not a function. So you cannot access it as a `Callable<class_Callable>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **print\_debug**(...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_method_print_debug>`

Like `@GlobalScope.print<class_@GlobalScope_method_print>`, but includes
the current stack frame when running with the debugger turned on.

The output in the console may look like the following:

    Test print
    At: res://test.gd:15:_process()

\*\*Note:\*\* Calling this function from a `Thread<class_Thread>` is not
supported. Doing so will instead print the thread ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **print\_stack**()
`🔗<class_@GDScript_method_print_stack>`

Prints a stack trace at the current code location. See also
`get_stack<class_@GDScript_method_get_stack>`.

The output in the console may look like the following:

    Frame 0 - res://test.gd:16 in function '_process'

\*\*Note:\*\* This function only works if the running instance is
connected to a debugging server (i.e. an editor instance).
`print_stack<class_@GDScript_method_print_stack>` will not work in
projects exported in release mode, or in projects exported in debug mode
if not connected to a debugging server.

\*\*Note:\*\* Calling this function from a `Thread<class_Thread>` is not
supported. Doing so will instead print the thread ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **range**(...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_@GDScript_method_range>`

Returns an array with the given range.
`range<class_@GDScript_method_range>` can be called in three ways:

`range(n: int)`: Starts from 0, increases by steps of 1, and stops
*before* `n`. The argument `n` is **exclusive**.

`range(b: int, n: int)`: Starts from `b`, increases by steps of 1, and
stops *before* `n`. The arguments `b` and `n` are **inclusive** and
**exclusive**, respectively.

`range(b: int, n: int, s: int)`: Starts from `b`, increases/decreases by
steps of `s`, and stops *before* `n`. The arguments `b` and `n` are
**inclusive** and **exclusive**, respectively. The argument `s` **can**
be negative, but not `0`. If `s` is `0`, an error message is printed.

`range<class_@GDScript_method_range>` converts all arguments to
`int<class_int>` before processing.

\*\*Note:\*\* Returns an empty array if no value meets the value
constraint (e.g. `range(2, 5, -1)` or `range(5, 5, 1)`).

\*\*Examples:\*\*

    print(range(4))        # Prints [0, 1, 2, 3]
    print(range(2, 5))     # Prints [2, 3, 4]
    print(range(0, 6, 2))  # Prints [0, 2, 4]
    print(range(4, 1, -1)) # Prints [4, 3, 2]

To iterate over an `Array<class_Array>` backwards, use:

    var array = [3, 6, 9]
    for i in range(array.size() - 1, -1, -1):
        print(array[i])

Output:

    9
    6
    3

To iterate over `float<class_float>`, convert them in the loop.

    for i in range (3, 0, -1):
        print(i / 10.0)

Output:

    0.3
    0.2
    0.1

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **type\_exists**(type:
`StringName<class_StringName>`) `🔗<class_@GDScript_method_type_exists>`

Returns `true` if the given `Object<class_Object>`-derived class exists
in `ClassDB<class_ClassDB>`. Note that `Variant<class_Variant>` data
types are not registered in `ClassDB<class_ClassDB>`.

    type_exists("Sprite2D") # Returns true
    type_exists("NonExistentClass") # Returns false
