github\_url  
hide

# EditorFileSystemImportFormatSupportQuery

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Used to query and configure import format support.

classref-introduction-group

## Description

This class is used to query and configure a certain import format. It is
used in conjunction with asset format import plugins.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_file\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileSystemImportFormatSupportQuery_private_method__get_file_extensions>`

Return the file extensions supported.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_active**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileSystemImportFormatSupportQuery_private_method__is_active>`

Return whether this importer is active.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_query**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileSystemImportFormatSupportQuery_private_method__query>`

Query support. Return false if import must not continue.
