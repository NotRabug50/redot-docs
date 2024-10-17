github\_url  
hide

# MobileVRInterface

**Inherits:** `XRInterface<class_XRInterface>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Generic mobile VR implementation.

classref-introduction-group

## Description

This is a generic mobile VR implementation where you need to provide
details about the phone and HMD used. It does not rely on any existing
framework. This is the most basic interface we have. For the best
effect, you need a mobile phone with a gyroscope and accelerometer.

Note that even though there is no positional tracking, the camera will
assume the headset is at a height of 1.85 meters. You can change this by
setting `eye_height<class_MobileVRInterface_property_eye_height>`.

You can initialize this interface as follows:

    var interface = XRServer.find_interface("Native mobile")
    if interface and interface.initialize():
        get_viewport().use_xr = true

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **display\_to\_lens** = `4.0`
`🔗<class_MobileVRInterface_property_display_to_lens>`

classref-property-setget

-   `void (No return value.)` **set\_display\_to\_lens**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_display\_to\_lens**()

The distance between the display and the lenses inside of the device in
centimeters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **display\_width** = `14.5`
`🔗<class_MobileVRInterface_property_display_width>`

classref-property-setget

-   `void (No return value.)` **set\_display\_width**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_display\_width**()

The width of the display in centimeters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **eye\_height** = `1.85`
`🔗<class_MobileVRInterface_property_eye_height>`

classref-property-setget

-   `void (No return value.)` **set\_eye\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_eye\_height**()

The height at which the camera is placed in relation to the ground (i.e.
`XROrigin3D<class_XROrigin3D>` node).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **iod** = `6.0`
`🔗<class_MobileVRInterface_property_iod>`

classref-property-setget

-   `void (No return value.)` **set\_iod**(value: `float<class_float>`)
-   `float<class_float>` **get\_iod**()

The interocular distance, also known as the interpupillary distance. The
distance between the pupils of the left and right eye.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **k1** = `0.215`
`🔗<class_MobileVRInterface_property_k1>`

classref-property-setget

-   `void (No return value.)` **set\_k1**(value: `float<class_float>`)
-   `float<class_float>` **get\_k1**()

The k1 lens factor is one of the two constants that define the strength
of the lens used and directly influences the lens distortion effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **k2** = `0.215`
`🔗<class_MobileVRInterface_property_k2>`

classref-property-setget

-   `void (No return value.)` **set\_k2**(value: `float<class_float>`)
-   `float<class_float>` **get\_k2**()

The k2 lens factor, see k1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2<class_Rect2>` **offset\_rect** = `Rect2(0, 0, 1, 1)`
`🔗<class_MobileVRInterface_property_offset_rect>`

classref-property-setget

-   `void (No return value.)` **set\_offset\_rect**(value:
    `Rect2<class_Rect2>`)
-   `Rect2<class_Rect2>` **get\_offset\_rect**()

Set the offset rect relative to the area being rendered. A length of 1
represents the whole rendering area on that axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **oversample** = `1.5`
`🔗<class_MobileVRInterface_property_oversample>`

classref-property-setget

-   `void (No return value.)` **set\_oversample**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_oversample**()

The oversample setting. Because of the lens distortion we have to render
our buffers at a higher resolution then the screen can natively handle.
A value between 1.5 and 2.0 often provides good results but at the cost
of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **vrs\_min\_radius** = `20.0`
`🔗<class_MobileVRInterface_property_vrs_min_radius>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_min\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vrs\_min\_radius**()

The minimum radius around the focal point where full quality is
guaranteed if VRS is used as a percentage of screen size.

\*\*Note:\*\* Mobile and Forward+ renderers only. Requires
`Viewport.vrs_mode<class_Viewport_property_vrs_mode>` to be set to
`Viewport.VRS_XR<class_Viewport_constant_VRS_XR>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **vrs\_strength** = `1.0`
`🔗<class_MobileVRInterface_property_vrs_strength>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vrs\_strength**()

The strength used to calculate the VRS density map. The greater this
value, the more noticeable VRS is. This improves performance at the cost
of quality.

\*\*Note:\*\* Mobile and Forward+ renderers only. Requires
`Viewport.vrs_mode<class_Viewport_property_vrs_mode>` to be set to
`Viewport.VRS_XR<class_Viewport_constant_VRS_XR>`.
