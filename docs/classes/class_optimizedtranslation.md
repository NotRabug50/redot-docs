github\_url  
hide

# OptimizedTranslation

**Inherits:** `Translation<class_Translation>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

An optimized translation, used by default for CSV Translations.

classref-introduction-group

## Description

An optimized translation, used by default for CSV Translations. Uses
real-time compressed translations, which results in very small
dictionaries.

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **generate**(from:
`Translation<class_Translation>`)
`🔗<class_OptimizedTranslation_method_generate>`

Generates and sets an optimized translation from the given
`Translation<class_Translation>` resource.

\*\*Note:\*\* This method is intended to be used in the editor. It does
nothing when called from an exported project.
