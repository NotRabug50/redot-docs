github\_url  
hide

# PolygonPathFinder

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

There is currently no description for this class. Please help us by
`contributing one <doc_updating_the_class_reference>`!

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

## Method Descriptions

classref-method

`PackedVector2Array<class_PackedVector2Array>` **find\_path**(from:
`Vector2<class_Vector2>`, to: `Vector2<class_Vector2>`)
`🔗<class_PolygonPathFinder_method_find_path>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_bounds**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PolygonPathFinder_method_get_bounds>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_closest\_point**(point:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PolygonPathFinder_method_get_closest_point>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_intersections**(from: `Vector2<class_Vector2>`, to:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PolygonPathFinder_method_get_intersections>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_point\_penalty**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PolygonPathFinder_method_get_point_penalty>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_point\_inside**(point:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PolygonPathFinder_method_is_point_inside>`

Returns `true` if `point` falls inside the polygon area.

gdscript

var polygon\_path\_finder = PolygonPathFinder.new() var points =
\[Vector2(0.0, 0.0), Vector2(1.0, 0.0), Vector2(0.0, 1.0)\] var
connections = \[0, 1, 1, 2, 2, 0\] polygon\_path\_finder.setup(points,
connections) print(polygon\_path\_finder.is\_point\_inside(Vector2(0.2,
0.2))) \# Prints true
print(polygon\_path\_finder.is\_point\_inside(Vector2(1.0, 1.0))) \#
Prints false

csharp

var polygonPathFinder = new PolygonPathFinder(); var points = new
Vector2\[\] { new Vector2(0.0f, 0.0f), new Vector2(1.0f, 0.0f), new
Vector2(0.0f, 1.0f) }; var connections = new int\[\] { 0, 1, 1, 2, 2, 0
}; polygonPathFinder.Setup(points, connections);
GD.Print(polygonPathFinder.IsPointInside(new Vector2(0.2f, 0.2f))); //
Prints true GD.Print(polygonPathFinder.IsPointInside(new Vector2(1.0f,
1.0f))); // Prints false

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_penalty**(idx: `int<class_int>`,
penalty: `float<class_float>`)
`🔗<class_PolygonPathFinder_method_set_point_penalty>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **setup**(points:
`PackedVector2Array<class_PackedVector2Array>`, connections:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_PolygonPathFinder_method_setup>`

Sets up **PolygonPathFinder** with an array of points that define the
vertices of the polygon, and an array of indices that determine the
edges of the polygon.

The length of `connections` must be even, returns an error if odd.

gdscript

var polygon\_path\_finder = PolygonPathFinder.new() var points =
\[Vector2(0.0, 0.0), Vector2(1.0, 0.0), Vector2(0.0, 1.0)\] var
connections = \[0, 1, 1, 2, 2, 0\] polygon\_path\_finder.setup(points,
connections)

csharp

var polygonPathFinder = new PolygonPathFinder(); var points = new
Vector2\[\] { new Vector2(0.0f, 0.0f), new Vector2(1.0f, 0.0f), new
Vector2(0.0f, 1.0f) }; var connections = new int\[\] { 0, 1, 1, 2, 2, 0
}; polygonPathFinder.Setup(points, connections);
