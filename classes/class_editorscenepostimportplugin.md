github\_url  
hide

# EditorScenePostImportPlugin

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Plugin to control and modifying the process of importing a scene.

classref-introduction-group

## Description

This plugin type exists to modify the process of importing scenes,
allowing to change the content as well as add importer options at every
stage of the process.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **InternalImportCategory**:
`🔗<enum_EditorScenePostImportPlugin_InternalImportCategory>`

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_NODE** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_MESH\_3D\_NODE** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_MESH** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_MATERIAL** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_ANIMATION** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_ANIMATION\_NODE** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_SKELETON\_3D\_NODE** = `6`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`InternalImportCategory<enum_EditorScenePostImportPlugin_InternalImportCategory>`
**INTERNAL\_IMPORT\_CATEGORY\_MAX** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_get\_import\_options**(path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorScenePostImportPlugin_private_method__get_import_options>`

Override to add general import options. These will appear in the main
import dock on the editor. Add options via
`add_import_option<class_EditorScenePostImportPlugin_method_add_import_option>`
and
`add_import_option_advanced<class_EditorScenePostImportPlugin_method_add_import_option_advanced>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_get\_internal\_import\_options**(category:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorScenePostImportPlugin_private_method__get_internal_import_options>`

Override to add internal import options. These will appear in the 3D
scene import dialog. Add options via
`add_import_option<class_EditorScenePostImportPlugin_method_add_import_option>`
and
`add_import_option_advanced<class_EditorScenePostImportPlugin_method_add_import_option_advanced>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>`
**\_get\_internal\_option\_update\_view\_required**(category:
`int<class_int>`, option: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorScenePostImportPlugin_private_method__get_internal_option_update_view_required>`

Return true whether updating the 3D view of the import dialog needs to
be updated if an option has changed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>`
**\_get\_internal\_option\_visibility**(category: `int<class_int>`,
for\_animation: `bool<class_bool>`, option: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorScenePostImportPlugin_private_method__get_internal_option_visibility>`

Return true or false whether a given option should be visible. Return
null to ignore.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_get\_option\_visibility**(path:
`String<class_String>`, for\_animation: `bool<class_bool>`, option:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorScenePostImportPlugin_private_method__get_option_visibility>`

Return true or false whether a given option should be visible. Return
null to ignore.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_internal\_process**(category:
`int<class_int>`, base\_node: `Node<class_Node>`, node:
`Node<class_Node>`, resource: `Resource<class_Resource>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorScenePostImportPlugin_private_method__internal_process>`

Process a specific node or resource for a given category.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_post\_process**(scene: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorScenePostImportPlugin_private_method__post_process>`

Post process the scene. This function is called after the final scene
has been configured.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_pre\_process**(scene: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorScenePostImportPlugin_private_method__pre_process>`

Pre Process the scene. This function is called right after the scene
format loader loaded the scene and no changes have been made.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_import\_option**(name:
`String<class_String>`, value: `Variant<class_Variant>`)
`🔗<class_EditorScenePostImportPlugin_method_add_import_option>`

Add a specific import option (name and default value only). This
function can only be called from
`_get_import_options<class_EditorScenePostImportPlugin_private_method__get_import_options>`
and
`_get_internal_import_options<class_EditorScenePostImportPlugin_private_method__get_internal_import_options>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_import\_option\_advanced**(type:
`Variant.Type<enum_@GlobalScope_Variant.Type>`, name:
`String<class_String>`, default\_value: `Variant<class_Variant>`, hint:
`PropertyHint<enum_@GlobalScope_PropertyHint>` = 0, hint\_string:
`String<class_String>` = "", usage\_flags: `int<class_int>` = 6)
`🔗<class_EditorScenePostImportPlugin_method_add_import_option_advanced>`

Add a specific import option. This function can only be called from
`_get_import_options<class_EditorScenePostImportPlugin_private_method__get_import_options>`
and
`_get_internal_import_options<class_EditorScenePostImportPlugin_private_method__get_internal_import_options>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_option\_value**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorScenePostImportPlugin_method_get_option_value>`

Query the value of an option. This function can only be called from
those querying visibility, or processing.
