github\_url  
hide

# Range

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `EditorSpinSlider<class_EditorSpinSlider>`,
`ProgressBar<class_ProgressBar>`, `ScrollBar<class_ScrollBar>`,
`Slider<class_Slider>`, `SpinBox<class_SpinBox>`,
`TextureProgressBar<class_TextureProgressBar>`

Abstract base class for controls that represent a number within a range.

classref-introduction-group

## Description

Range is an abstract base class for controls that represent a number
within a range, using a configured `step<class_Range_property_step>` and
`page<class_Range_property_page>` size. See e.g.
`ScrollBar<class_ScrollBar>` and `Slider<class_Slider>` for examples of
higher-level nodes using Range.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**changed**() `🔗<class_Range_signal_changed>`

Emitted when `min_value<class_Range_property_min_value>`,
`max_value<class_Range_property_max_value>`,
`page<class_Range_property_page>`, or `step<class_Range_property_step>`
change.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**value\_changed**(value: `float<class_float>`)
`🔗<class_Range_signal_value_changed>`

Emitted when `value<class_Range_property_value>` changes. When used on a
`Slider<class_Slider>`, this is called continuously while dragging
(potentially every frame). If you are performing an expensive operation
in a function connected to
`value_changed<class_Range_signal_value_changed>`, consider using a
*debouncing* `Timer<class_Timer>` to call the function less often.

\*\*Note:\*\* Unlike signals such as
`LineEdit.text_changed<class_LineEdit_signal_text_changed>`,
`value_changed<class_Range_signal_value_changed>` is also emitted when
`value` is set directly via code.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_greater** = `false`
`🔗<class_Range_property_allow_greater>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_greater**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_greater\_allowed**()

If `true`, `value<class_Range_property_value>` may be greater than
`max_value<class_Range_property_max_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **allow\_lesser** = `false`
`🔗<class_Range_property_allow_lesser>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_lesser**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_lesser\_allowed**()

If `true`, `value<class_Range_property_value>` may be less than
`min_value<class_Range_property_min_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **exp\_edit** = `false`
`🔗<class_Range_property_exp_edit>`

classref-property-setget

-   `void (No return value.)` **set\_exp\_ratio**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ratio\_exp**()

If `true`, and `min_value<class_Range_property_min_value>` is greater
than 0, `value<class_Range_property_value>` will be represented
exponentially rather than linearly.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_value** = `100.0`
`🔗<class_Range_property_max_value>`

classref-property-setget

-   `void (No return value.)` **set\_max**(value: `float<class_float>`)
-   `float<class_float>` **get\_max**()

Maximum value. Range is clamped if `value<class_Range_property_value>`
is greater than `max_value<class_Range_property_max_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_value** = `0.0`
`🔗<class_Range_property_min_value>`

classref-property-setget

-   `void (No return value.)` **set\_min**(value: `float<class_float>`)
-   `float<class_float>` **get\_min**()

Minimum value. Range is clamped if `value<class_Range_property_value>`
is less than `min_value<class_Range_property_min_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **page** = `0.0` `🔗<class_Range_property_page>`

classref-property-setget

-   `void (No return value.)` **set\_page**(value: `float<class_float>`)
-   `float<class_float>` **get\_page**()

Page size. Used mainly for `ScrollBar<class_ScrollBar>`. ScrollBar's
length is its size multiplied by `page<class_Range_property_page>` over
the difference between `min_value<class_Range_property_min_value>` and
`max_value<class_Range_property_max_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ratio** `🔗<class_Range_property_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_as\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_as\_ratio**()

The value mapped between 0 and 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **rounded** = `false`
`🔗<class_Range_property_rounded>`

classref-property-setget

-   `void (No return value.)` **set\_use\_rounded\_values**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_rounded\_values**()

If `true`, `value<class_Range_property_value>` will always be rounded to
the nearest integer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **step** = `0.01` `🔗<class_Range_property_step>`

classref-property-setget

-   `void (No return value.)` **set\_step**(value: `float<class_float>`)
-   `float<class_float>` **get\_step**()

If greater than 0, `value<class_Range_property_value>` will always be
rounded to a multiple of this property's value. If
`rounded<class_Range_property_rounded>` is also `true`,
`value<class_Range_property_value>` will first be rounded to a multiple
of this property's value, then rounded to the nearest integer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **value** = `0.0` `🔗<class_Range_property_value>`

classref-property-setget

-   `void (No return value.)` **set\_value**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_value**()

Range's current value. Changing this property (even via code) will
trigger `value_changed<class_Range_signal_value_changed>` signal. Use
`set_value_no_signal<class_Range_method_set_value_no_signal>` if you
want to avoid it.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_value\_changed**(new\_value:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Range_private_method__value_changed>`

Called when the **Range**'s value is changed (following the same
conditions as `value_changed<class_Range_signal_value_changed>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_value\_no\_signal**(value:
`float<class_float>`) `🔗<class_Range_method_set_value_no_signal>`

Sets the **Range**'s current value to the specified `value`, without
emitting the `value_changed<class_Range_signal_value_changed>` signal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **share**(with: `Node<class_Node>`)
`🔗<class_Range_method_share>`

Binds two **Range**s together along with any ranges previously grouped
with either of them. When any of range's member variables change, it
will share the new value with all other ranges in its group.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unshare**() `🔗<class_Range_method_unshare>`

Stops the **Range** from sharing its member variables with any other.
