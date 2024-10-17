github\_url  
hide

# FastNoiseLite

**Inherits:** `Noise<class_Noise>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Generates noise using the FastNoiseLite library.

classref-introduction-group

## Description

This class generates noise using the FastNoiseLite library, which is a
collection of several noise algorithms including Cellular, Perlin,
Value, and more.

Most generated noise values are in the range of `[-1, 1]`, but not
always. Some of the cellular noise algorithms return results above `1`.

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

enum **NoiseType**: `🔗<enum_FastNoiseLite_NoiseType>`

classref-enumeration-constant

`NoiseType<enum_FastNoiseLite_NoiseType>` **TYPE\_VALUE** = `5`

A lattice of points are assigned random values then interpolated based
on neighboring values.

classref-enumeration-constant

`NoiseType<enum_FastNoiseLite_NoiseType>` **TYPE\_VALUE\_CUBIC** = `4`

Similar to Value noise, but slower. Has more variance in peaks and
valleys.

Cubic noise can be used to avoid certain artifacts when using value
noise to create a bumpmap. In general, you should always use this mode
if the value noise is being used for a heightmap or bumpmap.

classref-enumeration-constant

`NoiseType<enum_FastNoiseLite_NoiseType>` **TYPE\_PERLIN** = `3`

A lattice of random gradients. Their dot products are interpolated to
obtain values in between the lattices.

classref-enumeration-constant

`NoiseType<enum_FastNoiseLite_NoiseType>` **TYPE\_CELLULAR** = `2`

Cellular includes both Worley noise and Voronoi diagrams which creates
various regions of the same value.

classref-enumeration-constant

`NoiseType<enum_FastNoiseLite_NoiseType>` **TYPE\_SIMPLEX** = `0`

As opposed to `TYPE_PERLIN<class_FastNoiseLite_constant_TYPE_PERLIN>`,
gradients exist in a simplex lattice rather than a grid lattice,
avoiding directional artifacts. Internally uses FastNoiseLite's
OpenSimplex2 noise type.

classref-enumeration-constant

`NoiseType<enum_FastNoiseLite_NoiseType>` **TYPE\_SIMPLEX\_SMOOTH** =
`1`

Modified, higher quality version of
`TYPE_SIMPLEX<class_FastNoiseLite_constant_TYPE_SIMPLEX>`, but slower.
Internally uses FastNoiseLite's OpenSimplex2S noise type.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FractalType**: `🔗<enum_FastNoiseLite_FractalType>`

classref-enumeration-constant

`FractalType<enum_FastNoiseLite_FractalType>` **FRACTAL\_NONE** = `0`

No fractal noise.

classref-enumeration-constant

`FractalType<enum_FastNoiseLite_FractalType>` **FRACTAL\_FBM** = `1`

Method using Fractional Brownian Motion to combine octaves into a
fractal.

classref-enumeration-constant

`FractalType<enum_FastNoiseLite_FractalType>` **FRACTAL\_RIDGED** = `2`

Method of combining octaves into a fractal resulting in a "ridged" look.

classref-enumeration-constant

`FractalType<enum_FastNoiseLite_FractalType>` **FRACTAL\_PING\_PONG** =
`3`

Method of combining octaves into a fractal with a ping pong effect.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CellularDistanceFunction**:
`🔗<enum_FastNoiseLite_CellularDistanceFunction>`

classref-enumeration-constant

`CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
**DISTANCE\_EUCLIDEAN** = `0`

Euclidean distance to the nearest point.

classref-enumeration-constant

`CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
**DISTANCE\_EUCLIDEAN\_SQUARED** = `1`

Squared Euclidean distance to the nearest point.

classref-enumeration-constant

`CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
**DISTANCE\_MANHATTAN** = `2`

Manhattan distance (taxicab metric) to the nearest point.

classref-enumeration-constant

`CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
**DISTANCE\_HYBRID** = `3`

Blend of
`DISTANCE_EUCLIDEAN<class_FastNoiseLite_constant_DISTANCE_EUCLIDEAN>`
and
`DISTANCE_MANHATTAN<class_FastNoiseLite_constant_DISTANCE_MANHATTAN>` to
give curved cell boundaries

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CellularReturnType**: `🔗<enum_FastNoiseLite_CellularReturnType>`

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_CELL\_VALUE** = `0`

The cellular distance function will return the same value for all points
within a cell.

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_DISTANCE** = `1`

The cellular distance function will return a value determined by the
distance to the nearest point.

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_DISTANCE2** = `2`

The cellular distance function returns the distance to the
second-nearest point.

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_DISTANCE2\_ADD** = `3`

The distance to the nearest point is added to the distance to the
second-nearest point.

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_DISTANCE2\_SUB** = `4`

The distance to the nearest point is subtracted from the distance to the
second-nearest point.

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_DISTANCE2\_MUL** = `5`

The distance to the nearest point is multiplied with the distance to the
second-nearest point.

classref-enumeration-constant

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**RETURN\_DISTANCE2\_DIV** = `6`

The distance to the nearest point is divided by the distance to the
second-nearest point.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DomainWarpType**: `🔗<enum_FastNoiseLite_DomainWarpType>`

classref-enumeration-constant

`DomainWarpType<enum_FastNoiseLite_DomainWarpType>`
**DOMAIN\_WARP\_SIMPLEX** = `0`

The domain is warped using the simplex noise algorithm.

classref-enumeration-constant

`DomainWarpType<enum_FastNoiseLite_DomainWarpType>`
**DOMAIN\_WARP\_SIMPLEX\_REDUCED** = `1`

The domain is warped using a simplified version of the simplex noise
algorithm.

classref-enumeration-constant

`DomainWarpType<enum_FastNoiseLite_DomainWarpType>`
**DOMAIN\_WARP\_BASIC\_GRID** = `2`

The domain is warped using a simple noise grid (not as smooth as the
other methods, but more performant).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DomainWarpFractalType**:
`🔗<enum_FastNoiseLite_DomainWarpFractalType>`

classref-enumeration-constant

`DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`
**DOMAIN\_WARP\_FRACTAL\_NONE** = `0`

No fractal noise for warping the space.

classref-enumeration-constant

`DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`
**DOMAIN\_WARP\_FRACTAL\_PROGRESSIVE** = `1`

Warping the space progressively, octave for octave, resulting in a more
"liquified" distortion.

classref-enumeration-constant

`DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`
**DOMAIN\_WARP\_FRACTAL\_INDEPENDENT** = `2`

Warping the space independently for each octave, resulting in a more
chaotic distortion.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
**cellular\_distance\_function** = `0`
`🔗<class_FastNoiseLite_property_cellular_distance_function>`

classref-property-setget

-   `void (No return value.)`
    **set\_cellular\_distance\_function**(value:
    `CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`)
-   `CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
    **get\_cellular\_distance\_function**()

Determines how the distance to the nearest/second-nearest point is
computed. See
`CellularDistanceFunction<enum_FastNoiseLite_CellularDistanceFunction>`
for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **cellular\_jitter** = `1.0`
`🔗<class_FastNoiseLite_property_cellular_jitter>`

classref-property-setget

-   `void (No return value.)` **set\_cellular\_jitter**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cellular\_jitter**()

Maximum distance a point can move off of its grid position. Set to `0`
for an even grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
**cellular\_return\_type** = `1`
`🔗<class_FastNoiseLite_property_cellular_return_type>`

classref-property-setget

-   `void (No return value.)` **set\_cellular\_return\_type**(value:
    `CellularReturnType<enum_FastNoiseLite_CellularReturnType>`)
-   `CellularReturnType<enum_FastNoiseLite_CellularReturnType>`
    **get\_cellular\_return\_type**()

Return type from cellular noise calculations. See
`CellularReturnType<enum_FastNoiseLite_CellularReturnType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **domain\_warp\_amplitude** = `30.0`
`🔗<class_FastNoiseLite_property_domain_warp_amplitude>`

classref-property-setget

-   `void (No return value.)` **set\_domain\_warp\_amplitude**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_domain\_warp\_amplitude**()

Sets the maximum warp distance from the origin.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **domain\_warp\_enabled** = `false`
`🔗<class_FastNoiseLite_property_domain_warp_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_domain\_warp\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_domain\_warp\_enabled**()

If enabled, another FastNoiseLite instance is used to warp the space,
resulting in a distortion of the noise.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **domain\_warp\_fractal\_gain** = `0.5`
`🔗<class_FastNoiseLite_property_domain_warp_fractal_gain>`

classref-property-setget

-   `void (No return value.)`
    **set\_domain\_warp\_fractal\_gain**(value: `float<class_float>`)
-   `float<class_float>` **get\_domain\_warp\_fractal\_gain**()

Determines the strength of each subsequent layer of the noise which is
used to warp the space.

A low value places more emphasis on the lower frequency base layers,
while a high value puts more emphasis on the higher frequency layers.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **domain\_warp\_fractal\_lacunarity** = `6.0`
`🔗<class_FastNoiseLite_property_domain_warp_fractal_lacunarity>`

classref-property-setget

-   `void (No return value.)`
    **set\_domain\_warp\_fractal\_lacunarity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_domain\_warp\_fractal\_lacunarity**()

Octave lacunarity of the fractal noise which warps the space. Increasing
this value results in higher octaves producing noise with finer details
and a rougher appearance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **domain\_warp\_fractal\_octaves** = `5`
`🔗<class_FastNoiseLite_property_domain_warp_fractal_octaves>`

classref-property-setget

-   `void (No return value.)`
    **set\_domain\_warp\_fractal\_octaves**(value: `int<class_int>`)
-   `int<class_int>` **get\_domain\_warp\_fractal\_octaves**()

The number of noise layers that are sampled to get the final value for
the fractal noise which warps the space.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`
**domain\_warp\_fractal\_type** = `1`
`🔗<class_FastNoiseLite_property_domain_warp_fractal_type>`

classref-property-setget

-   `void (No return value.)`
    **set\_domain\_warp\_fractal\_type**(value:
    `DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`)
-   `DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`
    **get\_domain\_warp\_fractal\_type**()

The method for combining octaves into a fractal which is used to warp
the space. See
`DomainWarpFractalType<enum_FastNoiseLite_DomainWarpFractalType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **domain\_warp\_frequency** = `0.05`
`🔗<class_FastNoiseLite_property_domain_warp_frequency>`

classref-property-setget

-   `void (No return value.)` **set\_domain\_warp\_frequency**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_domain\_warp\_frequency**()

Frequency of the noise which warps the space. Low frequency results in
smooth noise while high frequency results in rougher, more granular
noise.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DomainWarpType<enum_FastNoiseLite_DomainWarpType>`
**domain\_warp\_type** = `0`
`🔗<class_FastNoiseLite_property_domain_warp_type>`

classref-property-setget

-   `void (No return value.)` **set\_domain\_warp\_type**(value:
    `DomainWarpType<enum_FastNoiseLite_DomainWarpType>`)
-   `DomainWarpType<enum_FastNoiseLite_DomainWarpType>`
    **get\_domain\_warp\_type**()

Sets the warp algorithm. See
`DomainWarpType<enum_FastNoiseLite_DomainWarpType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fractal\_gain** = `0.5`
`🔗<class_FastNoiseLite_property_fractal_gain>`

classref-property-setget

-   `void (No return value.)` **set\_fractal\_gain**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fractal\_gain**()

Determines the strength of each subsequent layer of noise in fractal
noise.

A low value places more emphasis on the lower frequency base layers,
while a high value puts more emphasis on the higher frequency layers.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fractal\_lacunarity** = `2.0`
`🔗<class_FastNoiseLite_property_fractal_lacunarity>`

classref-property-setget

-   `void (No return value.)` **set\_fractal\_lacunarity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fractal\_lacunarity**()

Frequency multiplier between subsequent octaves. Increasing this value
results in higher octaves producing noise with finer details and a
rougher appearance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **fractal\_octaves** = `5`
`🔗<class_FastNoiseLite_property_fractal_octaves>`

classref-property-setget

-   `void (No return value.)` **set\_fractal\_octaves**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_fractal\_octaves**()

The number of noise layers that are sampled to get the final value for
fractal noise types.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fractal\_ping\_pong\_strength** = `2.0`
`🔗<class_FastNoiseLite_property_fractal_ping_pong_strength>`

classref-property-setget

-   `void (No return value.)`
    **set\_fractal\_ping\_pong\_strength**(value: `float<class_float>`)
-   `float<class_float>` **get\_fractal\_ping\_pong\_strength**()

Sets the strength of the fractal ping pong type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FractalType<enum_FastNoiseLite_FractalType>` **fractal\_type** = `1`
`🔗<class_FastNoiseLite_property_fractal_type>`

classref-property-setget

-   `void (No return value.)` **set\_fractal\_type**(value:
    `FractalType<enum_FastNoiseLite_FractalType>`)
-   `FractalType<enum_FastNoiseLite_FractalType>`
    **get\_fractal\_type**()

The method for combining octaves into a fractal. See
`FractalType<enum_FastNoiseLite_FractalType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fractal\_weighted\_strength** = `0.0`
`🔗<class_FastNoiseLite_property_fractal_weighted_strength>`

classref-property-setget

-   `void (No return value.)`
    **set\_fractal\_weighted\_strength**(value: `float<class_float>`)
-   `float<class_float>` **get\_fractal\_weighted\_strength**()

Higher weighting means higher octaves have less impact if lower octaves
have a large impact.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **frequency** = `0.01`
`🔗<class_FastNoiseLite_property_frequency>`

classref-property-setget

-   `void (No return value.)` **set\_frequency**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_frequency**()

The frequency for all noise types. Low frequency results in smooth noise
while high frequency results in rougher, more granular noise.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NoiseType<enum_FastNoiseLite_NoiseType>` **noise\_type** = `1`
`🔗<class_FastNoiseLite_property_noise_type>`

classref-property-setget

-   `void (No return value.)` **set\_noise\_type**(value:
    `NoiseType<enum_FastNoiseLite_NoiseType>`)
-   `NoiseType<enum_FastNoiseLite_NoiseType>` **get\_noise\_type**()

The noise algorithm used. See `NoiseType<enum_FastNoiseLite_NoiseType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **offset** = `Vector3(0, 0, 0)`
`🔗<class_FastNoiseLite_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_offset**()

Translate the noise input coordinates by the given
`Vector3<class_Vector3>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **seed** = `0` `🔗<class_FastNoiseLite_property_seed>`

classref-property-setget

-   `void (No return value.)` **set\_seed**(value: `int<class_int>`)
-   `int<class_int>` **get\_seed**()

The random number seed for all noise types.
