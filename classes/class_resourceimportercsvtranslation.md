github\_url  
hide

# ResourceImporterCSVTranslation

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports comma-separated values

classref-introduction-group

## Description

Comma-separated values are a plain text table storage format. The
format's simplicity makes it easy to edit in any text editor or
spreadsheet software. This makes it a common choice for game
localization.

\*\*Example CSV file:\*\*

    keys,en,es,ja
    GREET,"Hello, friend!","Hola, amigo!",こんにちは
    ASK,How are you?,Cómo está?,元気ですか
    BYE,Goodbye,Adiós,さようなら
    QUOTE,"""Hello"" said the man.","""Hola"" dijo el hombre.",「こんにちは」男は言いました

classref-introduction-group

## Tutorials

-   `Importing translations <../tutorials/assets_pipeline/importing_translations>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **compress** = `true`
`🔗<class_ResourceImporterCSVTranslation_property_compress>`

If `true`, creates an `OptimizedTranslation<class_OptimizedTranslation>`
instead of a `Translation<class_Translation>`. This makes the resulting
file smaller at the cost of a small CPU overhead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **delimiter** = `0`
`🔗<class_ResourceImporterCSVTranslation_property_delimiter>`

The delimiter to use in the CSV file. The default value matches the
common CSV convention. Tab-separated values are sometimes called TSV
files.
