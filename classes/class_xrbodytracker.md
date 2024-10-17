github\_url  
hide

# XRBodyTracker

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `XRPositionalTracker<class_XRPositionalTracker>` **&lt;**
`XRTracker<class_XRTracker>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A tracked body in XR.

classref-introduction-group

## Description

A body tracking system will create an instance of this object and add it
to the `XRServer<class_XRServer>`. This tracking system will then obtain
skeleton data, convert it to the Godot Humanoid skeleton and store this
data on the **XRBodyTracker** object.

Use `XRBodyModifier3D<class_XRBodyModifier3D>` to animate a body mesh
using body tracking data.

classref-introduction-group

## Tutorials

-   `XR documentation index <../tutorials/xr/index>`

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

flags **BodyFlags**: `🔗<enum_XRBodyTracker_BodyFlags>`

classref-enumeration-constant

`BodyFlags<enum_XRBodyTracker_BodyFlags>`
**BODY\_FLAG\_UPPER\_BODY\_SUPPORTED** = `1`

Upper body tracking supported.

classref-enumeration-constant

`BodyFlags<enum_XRBodyTracker_BodyFlags>`
**BODY\_FLAG\_LOWER\_BODY\_SUPPORTED** = `2`

Lower body tracking supported.

classref-enumeration-constant

`BodyFlags<enum_XRBodyTracker_BodyFlags>`
**BODY\_FLAG\_HANDS\_SUPPORTED** = `4`

Hand tracking supported.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Joint**: `🔗<enum_XRBodyTracker_Joint>`

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_ROOT** = `0`

Root joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_HIPS** = `1`

Hips joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_SPINE** = `2`

Spine joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_CHEST** = `3`

Chest joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_UPPER\_CHEST** = `4`

Upper chest joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_NECK** = `5`

Neck joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_HEAD** = `6`

Head joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_HEAD\_TIP** = `7`

Head tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_SHOULDER** = `8`

Left shoulder joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_UPPER\_ARM** = `9`

Left upper arm joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_LOWER\_ARM** = `10`

Left lower arm joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_SHOULDER** = `11`

Right shoulder joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_UPPER\_ARM** = `12`

Right upper arm joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_LOWER\_ARM** = `13`

Right lower arm joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_UPPER\_LEG** = `14`

Left upper leg joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_LOWER\_LEG** = `15`

Left lower leg joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_FOOT** = `16`

Left foot joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_TOES** = `17`

Left toes joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_UPPER\_LEG** = `18`

Right upper leg joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_LOWER\_LEG** = `19`

Right lower leg joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_FOOT** = `20`

Right foot joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_TOES** = `21`

Right toes joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_HAND** = `22`

Left hand joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_PALM** = `23`

Left palm joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_WRIST** = `24`

Left wrist joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_THUMB\_METACARPAL** =
`25`

Left thumb metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_THUMB\_PHALANX\_PROXIMAL** = `26`

Left thumb phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_THUMB\_PHALANX\_DISTAL** = `27`

Left thumb phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_THUMB\_TIP** = `28`

Left thumb tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_INDEX\_FINGER\_METACARPAL** = `29`

Left index finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_INDEX\_FINGER\_PHALANX\_PROXIMAL** = `30`

Left index finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_INDEX\_FINGER\_PHALANX\_INTERMEDIATE** = `31`

Left index finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_INDEX\_FINGER\_PHALANX\_DISTAL** = `32`

Left index finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_INDEX\_FINGER\_TIP** =
`33`

Left index finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_MIDDLE\_FINGER\_METACARPAL** = `34`

Left middle finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_MIDDLE\_FINGER\_PHALANX\_PROXIMAL** = `35`

Left middle finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_MIDDLE\_FINGER\_PHALANX\_INTERMEDIATE** = `36`

Left middle finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_MIDDLE\_FINGER\_PHALANX\_DISTAL** = `37`

Left middle finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_MIDDLE\_FINGER\_TIP** =
`38`

Left middle finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_RING\_FINGER\_METACARPAL** = `39`

Left ring finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_RING\_FINGER\_PHALANX\_PROXIMAL** = `40`

Left ring finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_RING\_FINGER\_PHALANX\_INTERMEDIATE** = `41`

Left ring finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_RING\_FINGER\_PHALANX\_DISTAL** = `42`

Left ring finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_RING\_FINGER\_TIP** =
`43`

Left ring finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_PINKY\_FINGER\_METACARPAL** = `44`

Left pinky finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_PINKY\_FINGER\_PHALANX\_PROXIMAL** = `45`

Left pinky finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_PINKY\_FINGER\_PHALANX\_INTERMEDIATE** = `46`

Left pinky finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_LEFT\_PINKY\_FINGER\_PHALANX\_DISTAL** = `47`

Left pinky finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_LEFT\_PINKY\_FINGER\_TIP** =
`48`

Left pinky finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_HAND** = `49`

Right hand joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_PALM** = `50`

Right palm joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_WRIST** = `51`

Right wrist joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_THUMB\_METACARPAL** =
`52`

Right thumb metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_THUMB\_PHALANX\_PROXIMAL** = `53`

Right thumb phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_THUMB\_PHALANX\_DISTAL** = `54`

Right thumb phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_THUMB\_TIP** = `55`

Right thumb tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_INDEX\_FINGER\_METACARPAL** = `56`

Right index finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_INDEX\_FINGER\_PHALANX\_PROXIMAL** = `57`

Right index finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_INDEX\_FINGER\_PHALANX\_INTERMEDIATE** = `58`

Right index finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_INDEX\_FINGER\_PHALANX\_DISTAL** = `59`

Right index finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_INDEX\_FINGER\_TIP** =
`60`

Right index finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_MIDDLE\_FINGER\_METACARPAL** = `61`

Right middle finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_MIDDLE\_FINGER\_PHALANX\_PROXIMAL** = `62`

Right middle finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_MIDDLE\_FINGER\_PHALANX\_INTERMEDIATE** = `63`

Right middle finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_MIDDLE\_FINGER\_PHALANX\_DISTAL** = `64`

Right middle finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_MIDDLE\_FINGER\_TIP**
= `65`

Right middle finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_RING\_FINGER\_METACARPAL** = `66`

Right ring finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_RING\_FINGER\_PHALANX\_PROXIMAL** = `67`

Right ring finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_RING\_FINGER\_PHALANX\_INTERMEDIATE** = `68`

Right ring finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_RING\_FINGER\_PHALANX\_DISTAL** = `69`

Right ring finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_RING\_FINGER\_TIP** =
`70`

Right ring finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_PINKY\_FINGER\_METACARPAL** = `71`

Right pinky finger metacarpal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_PINKY\_FINGER\_PHALANX\_PROXIMAL** = `72`

Right pinky finger phalanx proximal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_PINKY\_FINGER\_PHALANX\_INTERMEDIATE** = `73`

Right pinky finger phalanx intermediate joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>`
**JOINT\_RIGHT\_PINKY\_FINGER\_PHALANX\_DISTAL** = `74`

Right pinky finger phalanx distal joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_RIGHT\_PINKY\_FINGER\_TIP** =
`75`

Right pinky finger tip joint.

classref-enumeration-constant

`Joint<enum_XRBodyTracker_Joint>` **JOINT\_MAX** = `76`

Represents the size of the `Joint<enum_XRBodyTracker_Joint>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **JointFlags**: `🔗<enum_XRBodyTracker_JointFlags>`

classref-enumeration-constant

`JointFlags<enum_XRBodyTracker_JointFlags>`
**JOINT\_FLAG\_ORIENTATION\_VALID** = `1`

The joint's orientation data is valid.

classref-enumeration-constant

`JointFlags<enum_XRBodyTracker_JointFlags>`
**JOINT\_FLAG\_ORIENTATION\_TRACKED** = `2`

The joint's orientation is actively tracked. May not be set if tracking
has been temporarily lost.

classref-enumeration-constant

`JointFlags<enum_XRBodyTracker_JointFlags>`
**JOINT\_FLAG\_POSITION\_VALID** = `4`

The joint's position data is valid.

classref-enumeration-constant

`JointFlags<enum_XRBodyTracker_JointFlags>`
**JOINT\_FLAG\_POSITION\_TRACKED** = `8`

The joint's position is actively tracked. May not be set if tracking has
been temporarily lost.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`BodyFlags<enum_XRBodyTracker_BodyFlags>`\]
**body\_flags** = `0` `🔗<class_XRBodyTracker_property_body_flags>`

classref-property-setget

-   `void (No return value.)` **set\_body\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`BodyFlags<enum_XRBodyTracker_BodyFlags>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`BodyFlags<enum_XRBodyTracker_BodyFlags>`\]
    **get\_body\_flags**()

The type of body tracking data captured.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **has\_tracking\_data** = `false`
`🔗<class_XRBodyTracker_property_has_tracking_data>`

classref-property-setget

-   `void (No return value.)` **set\_has\_tracking\_data**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_has\_tracking\_data**()

If `true`, the body tracking data is valid.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JointFlags<enum_XRBodyTracker_JointFlags>`\]
**get\_joint\_flags**(joint: `Joint<enum_XRBodyTracker_Joint>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRBodyTracker_method_get_joint_flags>`

Returns flags about the validity of the tracking data for the given body
joint (see `JointFlags<enum_XRBodyTracker_JointFlags>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_joint\_transform**(joint:
`Joint<enum_XRBodyTracker_Joint>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRBodyTracker_method_get_joint_transform>`

Returns the transform for the given body joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_joint\_flags**(joint:
`Joint<enum_XRBodyTracker_Joint>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JointFlags<enum_XRBodyTracker_JointFlags>`\])
`🔗<class_XRBodyTracker_method_set_joint_flags>`

Sets flags about the validity of the tracking data for the given body
joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_joint\_transform**(joint:
`Joint<enum_XRBodyTracker_Joint>`, transform:
`Transform3D<class_Transform3D>`)
`🔗<class_XRBodyTracker_method_set_joint_transform>`

Sets the transform for the given body joint.
