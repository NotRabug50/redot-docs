# Using the SurfaceTool

The `SurfaceTool <class_surfacetool>` provides a useful interface for
constructing geometry. The interface is similar to the
`ImmediateMesh <class_ImmediateMesh>` class. You set each per-vertex
attribute (e.g. normal, uv, color) and then when you add a vertex it
captures the attributes.

The SurfaceTool also provides some useful helper functions like
`index()` and `generate_normals()`.

Attributes are added before each vertex is added:

.. code-tab:: gdscript GDScript

st.set\_normal() \# Overwritten by normal below. st.set\_normal() \#
Added to next vertex. st.set\_color() \# Added to next vertex.
st.add\_vertex() \# Captures normal and color above. st.set\_normal() \#
Normal never added to a vertex.

csharp

st.SetNormal(); // Overwritten by normal below. st.SetNormal(); // Added
to next vertex. st.SetColor(); // Added to next vertex. st.AddVertex();
// Captures normal and color above. st.SetNormal(); // Normal never
added to a vertex.

When finished generating your geometry with the
`SurfaceTool <class_surfacetool>` call `commit()` to finish generating
the mesh. If an `ArrayMesh <class_ArrayMesh>` is passed to `commit()`
then it appends a new surface to the end of the ArrayMesh. While if
nothing is passed in, `commit()` returns an ArrayMesh.

.. code-tab:: gdscript GDScript

st.commit(mesh) \# Or: var mesh = st.commit()

csharp

st.Commit(mesh); // Or: var mesh = st.Commit();

Code creates a triangle with indices

.. code-tab:: gdscript GDScript

var st = SurfaceTool.new()

st.begin(Mesh.PRIMITIVE\_TRIANGLES)

\# Prepare attributes for add\_vertex. st.set\_normal(Vector3(0, 0, 1))
st.set\_uv(Vector2(0, 0)) \# Call last for each vertex, adds the above
attributes. st.add\_vertex(Vector3(-1, -1, 0))

st.set\_normal(Vector3(0, 0, 1)) st.set\_uv(Vector2(0, 1))
st.add\_vertex(Vector3(-1, 1, 0))

st.set\_normal(Vector3(0, 0, 1)) st.set\_uv(Vector2(1, 1))
st.add\_vertex(Vector3(1, 1, 0))

\# Commit to a mesh. var mesh = st.commit()

csharp

var st = new SurfaceTool();

st.Begin(Mesh.PrimitiveType.Triangles);

// Prepare attributes for AddVertex. st.SetNormal(new Vector3(0, 0, 1));
st.SetUV(new Vector2(0, 0)); // Call last for each vertex, adds the
above attributes. st.AddVertex(new Vector3(-1, -1, 0));

st.SetNormal(new Vector3(0, 0, 1)); st.SetUV(new Vector2(0, 1));
st.AddVertex(new Vector3(-1, 1, 0));

st.SetNormal(new Vector3(0, 0, 1)); st.SetUV(new Vector2(1, 1));
st.AddVertex(new Vector3(1, 1, 0));

// Commit to a mesh. var mesh = st.Commit();

You can optionally add an index array, either by calling `add_index()`
and adding vertices to the index array or by calling `index()` which
shrinks the vertex array to remove duplicate vertices.

.. code-tab:: gdscript GDScript

\# Creates a quad from four corner vertices. \# add\_index does not need
to be called before add\_vertex. st.add\_index(0) st.add\_index(1)
st.add\_index(2)

st.add\_index(1) st.add\_index(3) st.add\_index(2)

\# Alternatively: st.index()

csharp

// Creates a quad from four corner vertices. // AddIndex does not need
to be called before AddVertex. st.AddIndex(0); st.AddIndex(1);
st.AddIndex(2);

st.AddIndex(1); st.AddIndex(3); st.AddIndex(2);

// Alternatively: st.Index();

Similarly, if you have an index array, but you want each vertex to be
unique (e.g. because you want to use unique normals or colors per face
instead of per-vertex), you can call `deindex()`.

.. code-tab:: gdscript GDScript

st.deindex()

csharp

st.Deindex();

If you don't add custom normals yourself, you can add them using
`generate_normals()`, which should be called after generating geometry
and before committing the mesh using `commit()` or `commit_to_arrays()`.
Calling `generate_normals(true)` will flip the resulting normals. As a
side note, `generate_normals()` only works if the primitive type is set
to `Mesh.PRIMITIVE_TRIANGLES`.

You may notice that normal mapping or other material properties look
broken on the generated mesh. This is because normal mapping
**requires** the mesh to feature *tangents*, which are separate from
*normals*. You can either add custom tangents manually, or generate them
automatically with `generate_tangents()`. This method requires that each
vertex have UVs and normals set already.

.. code-tab:: gdscript GDScript

st.generate\_normals() st.generate\_tangents()

csharp

st.GenerateNormals(); st.GenerateTangents();

By default, when generating normals, they will be calculated on a
per-face basis. If you want smooth vertex normals, when adding vertices,
call `add_smooth_group()`. `add_smooth_group()` needs to be called while
building the geometry, e.g. before the call to `add_vertex()` (if
non-indexed) or `add_index()` (if indexed).
