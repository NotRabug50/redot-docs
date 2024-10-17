article\_outdated  
True

# Binary serialization API

## Introduction

Godot has a serialization API based on Variant. It's used for converting
data types to an array of bytes efficiently. This API is exposed via the
global `bytes_to_var() <class_@GlobalScope_method_bytes_to_var>` and
`var_to_bytes() <class_@GlobalScope_method_var_to_bytes>` functions, but
it is also used in the `get_var` and `store_var` methods of
`class_FileAccess` as well as the packet APIs for `class_PacketPeer`.
This format is *not* used for binary scenes and resources.

## Full Objects vs Object instance IDs

If a variable is serialized with `full_objects = true`, then any Objects
contained in the variable will be serialized and included in the result.
This is recursive.

If `full_objects = false`, then only the instance IDs will be serialized
for any Objects contained in the variable.

## Packet specification

The packet is designed to be always padded to 4 bytes. All values are
little-endian-encoded. All packets have a 4-byte header representing an
integer, specifying the type of data.

The lowest value two bytes are used to determine the type, while the
highest value two bytes contain flags:

    base_type = val & 0xFFFF;
    flags = val >> 16;

<table style="width:50%;">
<colgroup>
<col style="width: 12%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Type</th>
<th>Value</th>
</tr>
</thead>
<tbody>
<tr>
<td>0</td>
<td>null</td>
</tr>
<tr>
<td>1</td>
<td>bool</td>
</tr>
<tr>
<td>2</td>
<td>integer</td>
</tr>
<tr>
<td>3</td>
<td>float</td>
</tr>
<tr>
<td>4</td>
<td>string</td>
</tr>
<tr>
<td>5</td>
<td>vector2</td>
</tr>
<tr>
<td>6</td>
<td>rect2</td>
</tr>
<tr>
<td>7</td>
<td>vector3</td>
</tr>
<tr>
<td>8</td>
<td>transform2d</td>
</tr>
<tr>
<td>9</td>
<td>plane</td>
</tr>
<tr>
<td>10</td>
<td>quaternion</td>
</tr>
<tr>
<td>11</td>
<td>aabb</td>
</tr>
<tr>
<td>12</td>
<td>basis</td>
</tr>
<tr>
<td>13</td>
<td>transform3d</td>
</tr>
<tr>
<td>14</td>
<td>color</td>
</tr>
<tr>
<td>15</td>
<td>node path</td>
</tr>
<tr>
<td>16</td>
<td>rid</td>
</tr>
<tr>
<td>17</td>
<td>object</td>
</tr>
<tr>
<td>18</td>
<td>dictionary</td>
</tr>
<tr>
<td>19</td>
<td>array</td>
</tr>
<tr>
<td>20</td>
<td>raw array</td>
</tr>
<tr>
<td>21</td>
<td>int32 array</td>
</tr>
<tr>
<td>22</td>
<td>int64 array</td>
</tr>
<tr>
<td>23</td>
<td>float32 array</td>
</tr>
<tr>
<td>24</td>
<td>float64 array</td>
</tr>
<tr>
<td>25</td>
<td>string array</td>
</tr>
<tr>
<td>26</td>
<td>vector2 array</td>
</tr>
<tr>
<td>27</td>
<td>vector3 array</td>
</tr>
<tr>
<td>28</td>
<td>color array</td>
</tr>
<tr>
<td>29</td>
<td>max</td>
</tr>
</tbody>
</table>

Following this is the actual packet contents, which varies for each type
of packet. Note that this assumes Godot is compiled with
single-precision floats, which is the default. If Godot was compiled
with double-precision floats, the length of "Float" fields within data
structures should be 8, and the offset should be `(offset - 4) * 2 + 4`.
The "float" type itself always uses double precision.

### 0: null

### 1: `bool<class_bool>`

<table style="width:82%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 38%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>0 for False, 1 for True</td>
</tr>
</tbody>
</table>

### 2: `int<class_int>`

If no flags are set (flags == 0), the integer is sent as a 32 bit
integer:

<table style="width:81%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>32-bit signed integer</td>
</tr>
</tbody>
</table>

If flag `ENCODE_FLAG_64` is set (`flags & 1 == 1`), the integer is sent
as a 64-bit integer:

<table style="width:81%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>8</td>
<td>Integer</td>
<td>64-bit signed integer</td>
</tr>
</tbody>
</table>

### 3: `float<class_float>`

If no flags are set (flags == 0), the float is sent as a 32 bit single
precision:

<table style="width:90%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>IEEE 754 single-precision float</td>
</tr>
</tbody>
</table>

If flag `ENCODE_FLAG_64` is set (`flags & 1 == 1`), the float is sent as
a 64-bit double precision number:

<table style="width:90%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>8</td>
<td>Float</td>
<td>IEEE 754 double-precision float</td>
</tr>
</tbody>
</table>

### 4: `String<class_string>`

<table style="width:83%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 40%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>String length (in bytes)</td>
</tr>
<tr>
<td>8</td>
<td>X</td>
<td>Bytes</td>
<td>UTF-8 encoded string</td>
</tr>
</tbody>
</table>

This field is padded to 4 bytes.

### 5: `Vector2<class_vector2>`

<table style="width:64%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>X coordinate</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Y coordinate</td>
</tr>
</tbody>
</table>

### 6: `Rect2<class_rect2>`

<table style="width:64%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>X coordinate</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Y coordinate</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>X size</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>Y size</td>
</tr>
</tbody>
</table>

### 7: `Vector3<class_vector3>`

<table style="width:64%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>X coordinate</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Y coordinate</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>Z coordinate</td>
</tr>
</tbody>
</table>

### 8: `Transform2D<class_transform2d>`

<table style="width:98%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 10%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>The X component of the X column vector, accessed via [0][0]</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the X column vector, accessed via [0][1]</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>The X component of the Y column vector, accessed via [1][0]</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the Y column vector, accessed via [1][1]</td>
</tr>
<tr>
<td>20</td>
<td>4</td>
<td>Float</td>
<td>The X component of the origin vector, accessed via [2][0]</td>
</tr>
<tr>
<td>24</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the origin vector, accessed via [2][1]</td>
</tr>
</tbody>
</table>

### 9: `Plane<class_plane>`

<table style="width:62%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>Normal X</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Normal Y</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>Normal Z</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>Distance</td>
</tr>
</tbody>
</table>

### 10: `Quaternion<class_quaternion>`

<table style="width:62%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 22%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>Imaginary X</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Imaginary Y</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>Imaginary Z</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>Real W</td>
</tr>
</tbody>
</table>

### 11: `AABB<class_aabb>`

<table style="width:64%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>X coordinate</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Y coordinate</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>Z coordinate</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>X size</td>
</tr>
<tr>
<td>20</td>
<td>4</td>
<td>Float</td>
<td>Y size</td>
</tr>
<tr>
<td>24</td>
<td>4</td>
<td>Float</td>
<td>Z size</td>
</tr>
</tbody>
</table>

### 12: `Basis<class_basis>`

<table style="width:98%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 10%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>The X component of the X column vector, accessed via [0][0]</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the X column vector, accessed via [0][1]</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the X column vector, accessed via [0][2]</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>The X component of the Y column vector, accessed via [1][0]</td>
</tr>
<tr>
<td>20</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the Y column vector, accessed via [1][1]</td>
</tr>
<tr>
<td>24</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the Y column vector, accessed via [1][2]</td>
</tr>
<tr>
<td>28</td>
<td>4</td>
<td>Float</td>
<td>The X component of the Z column vector, accessed via [2][0]</td>
</tr>
<tr>
<td>32</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the Z column vector, accessed via [2][1]</td>
</tr>
<tr>
<td>36</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the Z column vector, accessed via [2][2]</td>
</tr>
</tbody>
</table>

### 13: `Transform3D<class_transform3d>`

<table style="width:98%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 10%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>The X component of the X column vector, accessed via [0][0]</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the X column vector, accessed via [0][1]</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the X column vector, accessed via [0][2]</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>The X component of the Y column vector, accessed via [1][0]</td>
</tr>
<tr>
<td>20</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the Y column vector, accessed via [1][1]</td>
</tr>
<tr>
<td>24</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the Y column vector, accessed via [1][2]</td>
</tr>
<tr>
<td>28</td>
<td>4</td>
<td>Float</td>
<td>The X component of the Z column vector, accessed via [2][0]</td>
</tr>
<tr>
<td>32</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the Z column vector, accessed via [2][1]</td>
</tr>
<tr>
<td>36</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the Z column vector, accessed via [2][2]</td>
</tr>
<tr>
<td>40</td>
<td>4</td>
<td>Float</td>
<td>The X component of the origin vector, accessed via [3][0]</td>
</tr>
<tr>
<td>44</td>
<td>4</td>
<td>Float</td>
<td>The Y component of the origin vector, accessed via [3][1]</td>
</tr>
<tr>
<td>48</td>
<td>4</td>
<td>Float</td>
<td>The Z component of the origin vector, accessed via [3][2]</td>
</tr>
</tbody>
</table>

### 14: `Color<class_color>`

<table style="width:98%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 10%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Float</td>
<td>Red (typically 0..1, can be above 1 for overbright colors)</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Float</td>
<td>Green (typically 0..1, can be above 1 for overbright colors)</td>
</tr>
<tr>
<td>12</td>
<td>4</td>
<td>Float</td>
<td>Blue (typically 0..1, can be above 1 for overbright colors)</td>
</tr>
<tr>
<td>16</td>
<td>4</td>
<td>Float</td>
<td>Alpha (0..1)</td>
</tr>
</tbody>
</table>

### 15: `NodePath<class_nodepath>`

<table style="width:98%;">
<colgroup>
<col style="width: 8%" />
<col style="width: 6%" />
<col style="width: 9%" />
<col style="width: 73%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>String length, or new format (val&amp;0x80000000!=0 and
NameCount=val&amp;0x7FFFFFFF)</td>
</tr>
</tbody>
</table>

### For old format:

<table style="width:75%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 13%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>8</td>
<td>X</td>
<td>Bytes</td>
<td>UTF-8 encoded string</td>
</tr>
</tbody>
</table>

Padded to 4 bytes.

### For new format:

<table style="width:96%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 52%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Sub-name count</td>
</tr>
<tr>
<td>8</td>
<td>4</td>
<td>Integer</td>
<td>Flags (absolute: val&amp;1 != 0 )</td>
</tr>
</tbody>
</table>

For each Name and Sub-Name

<table style="width:78%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>X+0</td>
<td>4</td>
<td>Integer</td>
<td>String length</td>
</tr>
<tr>
<td>X+4</td>
<td>X</td>
<td>Bytes</td>
<td>UTF-8 encoded string</td>
</tr>
</tbody>
</table>

Every name string is padded to 4 bytes.

### 16: `RID<class_rid>` (unsupported)

### 17: `Object<class_object>`

An Object could be serialized in three different ways: as a null value,
with `full_objects = false`, or with `full_objects = true`.

#### A null value

<table style="width:98%;">
<colgroup>
<col style="width: 13%" />
<col style="width: 9%" />
<col style="width: 15%" />
<col style="width: 59%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Zero (32-bit signed integer)</td>
</tr>
</tbody>
</table>

#### `full_objects` disabled

<table style="width:98%;">
<colgroup>
<col style="width: 13%" />
<col style="width: 9%" />
<col style="width: 15%" />
<col style="width: 59%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>8</td>
<td>Integer</td>
<td>The Object instance ID (64-bit signed integer)</td>
</tr>
</tbody>
</table>

#### `full_objects` enabled

<table style="width:98%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 17%" />
<col style="width: 60%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Class name (String length)</td>
</tr>
<tr>
<td>8</td>
<td>X</td>
<td>Bytes</td>
<td>Class name (UTF-8 encoded string)</td>
</tr>
<tr>
<td>X+8</td>
<td>4</td>
<td>Integer</td>
<td>The number of properties that are serialized</td>
</tr>
</tbody>
</table>

For each property:

<table style="width:98%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 8%" />
<col style="width: 17%" />
<col style="width: 60%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>Y</td>
<td>4</td>
<td>Integer</td>
<td>Property name (String length)</td>
</tr>
<tr>
<td>Y+4</td>
<td>Z</td>
<td>Bytes</td>
<td>Property name (UTF-8 encoded string)</td>
</tr>
<tr>
<td>Y+4+Z</td>
<td>W</td>
<td>&lt;variable&gt;</td>
<td>Property value, using this same format</td>
</tr>
</tbody>
</table>

Note

Not all properties are included. Only properties that are configured
with the
`PROPERTY_USAGE_STORAGE<class_@GlobalScope_constant_PROPERTY_USAGE_STORAGE>`
flag set will be serialized. You can add a new usage flag to a property
by overriding the
`_get_property_list<class_Object_private_method__get_property_list>`
method in your class. You can also check how property usage is
configured by calling `Object._get_property_list` See
`PropertyUsageFlags<enum_@GlobalScope_PropertyUsageFlags>` for the
possible usage flags.

### 18: `Dictionary<class_dictionary>`

<table style="width:98%;">
<colgroup>
<col style="width: 10%" />
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>val&amp;0x7FFFFFFF = elements, val&amp;0x80000000 = shared
(bool)</td>
</tr>
</tbody>
</table>

Then what follows is, for amount of "elements", pairs of key and value,
one after the other, using this same format.

### 19: `Array<class_array>`

<table style="width:98%;">
<colgroup>
<col style="width: 10%" />
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>val&amp;0x7FFFFFFF = elements, val&amp;0x80000000 = shared
(bool)</td>
</tr>
</tbody>
</table>

Then what follows is, for amount of "elements", values one after the
other, using this same format.

### 20: `PackedByteArray<class_PackedByteArray>`

<table style="width:85%;">
<colgroup>
<col style="width: 22%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length (Bytes)</td>
</tr>
<tr>
<td>8..8+length</td>
<td>1</td>
<td>Byte</td>
<td>Byte (0..255)</td>
</tr>
</tbody>
</table>

The array data is padded to 4 bytes.

### 21: `PackedInt32Array<class_PackedInt32Array>`

<table style="width:93%;">
<colgroup>
<col style="width: 26%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 38%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length (Integers)</td>
</tr>
<tr>
<td>8..8+length*4</td>
<td>4</td>
<td>Integer</td>
<td>32-bit signed integer</td>
</tr>
</tbody>
</table>

### 22: `PackedInt64Array<class_PackedInt64Array>`

<table style="width:93%;">
<colgroup>
<col style="width: 26%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 38%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>8</td>
<td>Integer</td>
<td>Array length (Integers)</td>
</tr>
<tr>
<td>8..8+length*8</td>
<td>8</td>
<td>Integer</td>
<td>64-bit signed integer</td>
</tr>
</tbody>
</table>

### 23: `PackedFloat32Array<class_PackedFloat32Array>`

<table style="width:98%;">
<colgroup>
<col style="width: 22%" />
<col style="width: 9%" />
<col style="width: 14%" />
<col style="width: 51%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length (Floats)</td>
</tr>
<tr>
<td>8..8+length*4</td>
<td>4</td>
<td>Integer</td>
<td>32-bit IEEE 754 single-precision float</td>
</tr>
</tbody>
</table>

### 24: `PackedFloat64Array<class_PackedFloat64Array>`

<table style="width:98%;">
<colgroup>
<col style="width: 22%" />
<col style="width: 9%" />
<col style="width: 14%" />
<col style="width: 51%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length (Floats)</td>
</tr>
<tr>
<td>8..8+length*8</td>
<td>8</td>
<td>Integer</td>
<td>64-bit IEEE 754 double-precision float</td>
</tr>
</tbody>
</table>

### 25: `PackedStringArray<class_PackedStringArray>`

<table style="width:81%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 37%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length (Strings)</td>
</tr>
</tbody>
</table>

For each String:

<table style="width:78%;">
<colgroup>
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 34%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>X+0</td>
<td>4</td>
<td>Integer</td>
<td>String length</td>
</tr>
<tr>
<td>X+4</td>
<td>X</td>
<td>Bytes</td>
<td>UTF-8 encoded string</td>
</tr>
</tbody>
</table>

Every string is padded to 4 bytes.

### 26: `PackedVector2Array<class_PackedVector2Array>`

<table style="width:79%;">
<colgroup>
<col style="width: 27%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length</td>
</tr>
<tr>
<td>8..8+length*8</td>
<td>4</td>
<td>Float</td>
<td>X coordinate</td>
</tr>
<tr>
<td>8..12+length*8</td>
<td>4</td>
<td>Float</td>
<td>Y coordinate</td>
</tr>
</tbody>
</table>

### 27: `PackedVector3Array<class_PackedVector3Array>`

<table style="width:81%;">
<colgroup>
<col style="width: 29%" />
<col style="width: 11%" />
<col style="width: 16%" />
<col style="width: 23%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length</td>
</tr>
<tr>
<td>8..8+length*12</td>
<td>4</td>
<td>Float</td>
<td>X coordinate</td>
</tr>
<tr>
<td>8..12+length*12</td>
<td>4</td>
<td>Float</td>
<td>Y coordinate</td>
</tr>
<tr>
<td>8..16+length*12</td>
<td>4</td>
<td>Float</td>
<td>Z coordinate</td>
</tr>
</tbody>
</table>

### 28: `PackedColorArray<class_PackedColorArray>`

<table style="width:98%;">
<colgroup>
<col style="width: 19%" />
<col style="width: 7%" />
<col style="width: 11%" />
<col style="width: 59%" />
</colgroup>
<thead>
<tr>
<th>Offset</th>
<th>Len</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>4</td>
<td>4</td>
<td>Integer</td>
<td>Array length</td>
</tr>
<tr>
<td>8..8+length*16</td>
<td>4</td>
<td>Float</td>
<td>Red (typically 0..1, can be above 1 for overbright colors)</td>
</tr>
<tr>
<td>8..12+length*16</td>
<td>4</td>
<td>Float</td>
<td>Green (typically 0..1, can be above 1 for overbright colors)</td>
</tr>
<tr>
<td>8..16+length*16</td>
<td>4</td>
<td>Float</td>
<td>Blue (typically 0..1, can be above 1 for overbright colors)</td>
</tr>
<tr>
<td>8..20+length*16</td>
<td>4</td>
<td>Float</td>
<td>Alpha (0..1)</td>
</tr>
</tbody>
</table>
