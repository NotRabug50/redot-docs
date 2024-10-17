github\_url  
hide

# OggPacketSequence

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A sequence of Ogg packets.

classref-introduction-group

## Description

A sequence of Ogg packets.

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
</tbody>
</table>

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

## Property Descriptions

classref-property

`PackedInt64Array<class_PackedInt64Array>` **granule\_positions** =
`PackedInt64Array()`
`🔗<class_OggPacketSequence_property_granule_positions>`

classref-property-setget

-   `void (No return value.)` **set\_packet\_granule\_positions**(value:
    `PackedInt64Array<class_PackedInt64Array>`)
-   `PackedInt64Array<class_PackedInt64Array>`
    **get\_packet\_granule\_positions**()

Contains the granule positions for each page in this packet sequence.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedInt64Array<class_PackedInt64Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`Array<class_Array>`\] **packet\_data** = `[]`
`🔗<class_OggPacketSequence_property_packet_data>`

classref-property-setget

-   `void (No return value.)` **set\_packet\_data**(value:
    `Array<class_Array>`\[`Array<class_Array>`\])
-   `Array<class_Array>`\[`Array<class_Array>`\] **get\_packet\_data**()

Contains the raw packets that make up this OggPacketSequence.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sampling\_rate** = `0.0`
`🔗<class_OggPacketSequence_property_sampling_rate>`

classref-property-setget

-   `void (No return value.)` **set\_sampling\_rate**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sampling\_rate**()

Holds sample rate information about this sequence. Must be set by
another class that actually understands the codec.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OggPacketSequence_method_get_length>`

The length of this stream, in seconds.
