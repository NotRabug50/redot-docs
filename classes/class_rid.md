github\_url  
hide

# RID

A handle for a `Resource<class_Resource>`'s unique identifier.

classref-introduction-group

## Description

The RID `Variant<class_Variant>` type is used to access a low-level
resource by its unique ID. RIDs are opaque, which means they do not
grant access to the resource by themselves. They are used by the
low-level server classes, such as `DisplayServer<class_DisplayServer>`,
`RenderingServer<class_RenderingServer>`,
`TextServer<class_TextServer>`, etc.

A low-level resource may correspond to a high-level
`Resource<class_Resource>`, such as `Texture<class_Texture>` or
`Mesh<class_Mesh>`.

\*\*Note:\*\* RIDs are only useful during the current session. It won't
correspond to a similar resource if sent over a network, or loaded from
a file at a later time.

Note

There are notable differences when using this API with C#. See
`doc_c_sharp_differences` for more information.

classref-reftable-group

## Constructors

<table>
<tbody>
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
</tbody>
</table>

classref-reftable-group

## Operators

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`RID<class_RID>` **RID**() `🔗<class_RID_constructor_RID>`

Constructs an empty **RID** with the invalid ID `0`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`RID<class_RID>` **RID**(from: `RID<class_RID>`)

Constructs a **RID** as a copy of the given **RID**.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RID_method_get_id>`

Returns the ID of the referenced low-level resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RID_method_is_valid>`

Returns `true` if the **RID** is not `0`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right: `RID<class_RID>`)
`🔗<class_RID_operator_neq_RID>`

Returns `true` if the **RID**s are not equal.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;**(right: `RID<class_RID>`)
`🔗<class_RID_operator_lt_RID>`

Returns `true` if the **RID**'s ID is less than `right`'s ID.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;=**(right: `RID<class_RID>`)
`🔗<class_RID_operator_lte_RID>`

Returns `true` if the **RID**'s ID is less than or equal to `right`'s
ID.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right: `RID<class_RID>`)
`🔗<class_RID_operator_eq_RID>`

Returns `true` if both **RID**s are equal, which means they both refer
to the same low-level resource.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;**(right: `RID<class_RID>`)
`🔗<class_RID_operator_gt_RID>`

Returns `true` if the **RID**'s ID is greater than `right`'s ID.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;=**(right: `RID<class_RID>`)
`🔗<class_RID_operator_gte_RID>`

Returns `true` if the **RID**'s ID is greater than or equal to `right`'s
ID.
