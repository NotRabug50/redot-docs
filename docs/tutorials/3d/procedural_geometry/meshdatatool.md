# Using the MeshDataTool

The `MeshDataTool <class_meshdatatool>` is not used to generate
geometry. But it is helpful for dynamically altering geometry, for
example if you want to write a script to tessellate, simplify, or deform
meshes.

The MeshDataTool is not as fast as altering arrays directly using
ArrayMesh. However, it provides more information and tools to work with
meshes than the ArrayMesh does. When the MeshDataTool is used, it
calculates mesh data that is not available in ArrayMeshes such as faces
and edges, which are necessary for certain mesh algorithms. If you do
not need this extra information then it may be better to use an
ArrayMesh.

Note

MeshDataTool can only be used on Meshes that use the PrimitiveType
`Mesh.PRIMITIVE_TRIANGLES`.

We initialize the MeshDataTool from an ArrayMesh by calling
`create_from_surface()`. If there is already data initialized in the
MeshDataTool, calling `create_from_surface()` will clear it for you.
Alternatively, you can call `clear()` yourself before re-using the
MeshDataTool.

In the examples below, assume an ArrayMesh called `mesh` has already
been created. See `ArrayMesh tutorial <doc_arraymesh>` for an example of
mesh generation.

.. code-tab:: gdscript GDScript

var mdt = MeshDataTool.new() mdt.create\_from\_surface(mesh, 0)

`create_from_surface()` uses the vertex arrays from the ArrayMesh to
calculate two additional arrays, one for edges and one for faces, for a
total of three arrays.

An edge is a connection between any two vertices. Each edge in the edge
array contains a reference to the two vertices it is composed of, and up
to two faces that it is contained within.

A face is a triangle made up of three vertices and three corresponding
edges. Each face in the face array contains a reference to the three
vertices and three edges it is composed of.

The vertex array contains edge, face, normal, color, tangent, uv, uv2,
bone, and weight information connected with each vertex.

To access information from these arrays you use a function of the form
`get_****()`:

.. code-tab:: gdscript GDScript

mdt.get\_vertex\_count() \# Returns number of vertices in vertex array.
mdt.get\_vertex\_faces(0) \# Returns array of faces that contain
vertex\[0\]. mdt.get\_face\_normal(1) \# Calculates and returns face
normal of the second face. mdt.get\_edge\_vertex(10, 1) \# Returns the
second vertex comprising the edge at index 10.

What you choose to do with these functions is up to you. A common use
case is to iterate over all vertices and transform them in some way:

.. code-tab:: gdscript GDScript

for i in range(get\_vertex\_count):  
var vert = mdt.get\_vertex(i) vert \*= 2.0 \# Scales the vertex by
doubling size. mdt.set\_vertex(i, vert)

These modifications are not done in place on the ArrayMesh. If you are
dynamically updating an existing ArrayMesh, first delete the existing
surface before adding a new one using
`commit_to_surface() <class_meshdatatool_method_commit_to_surface>`:

.. code-tab:: gdscript GDScript

mesh.clear\_surfaces() \# Deletes all of the mesh's surfaces.
mdt.commit\_to\_surface(mesh)

Below is a complete example that turns a spherical mesh called `mesh`
into a randomly deformed blob complete with updated normals and vertex
colors. See `ArrayMesh tutorial <doc_arraymesh>` for how to generate the
base mesh.

.. code-tab:: gdscript GDScript

extends MeshInstance3D

var fnl = FastNoiseLite.new() var mdt = MeshDataTool.new()

func \_ready():  
fnl.frequency = 0.7

mdt.create\_from\_surface(mesh, 0)

for i in range(mdt.get\_vertex\_count()):  
var vertex = mdt.get\_vertex(i).normalized() \# Push out vertex by
noise. vertex = vertex \* (fnl.get\_noise\_3dv(vertex) \* 0.5 + 0.75)
mdt.set\_vertex(i, vertex)

\# Calculate vertex normals, face-by-face. for i in
range(mdt.get\_face\_count()): \# Get the index in the vertex array. var
a = mdt.get\_face\_vertex(i, 0) var b = mdt.get\_face\_vertex(i, 1) var
c = mdt.get\_face\_vertex(i, 2) \# Get vertex position using vertex
index. var ap = mdt.get\_vertex(a) var bp = mdt.get\_vertex(b) var cp =
mdt.get\_vertex(c) \# Calculate face normal. var n = (bp -
cp).cross(ap - bp).normalized() \# Add face normal to current vertex
normal. \# This will not result in perfect normals, but it will be
close. mdt.set\_vertex\_normal(a, n + mdt.get\_vertex\_normal(a))
mdt.set\_vertex\_normal(b, n + mdt.get\_vertex\_normal(b))
mdt.set\_vertex\_normal(c, n + mdt.get\_vertex\_normal(c))

\# Run through vertices one last time to normalize normals and \# set
color to normal. for i in range(mdt.get\_vertex\_count()): var v =
mdt.get\_vertex\_normal(i).normalized() mdt.set\_vertex\_normal(i, v)
mdt.set\_vertex\_color(i, Color(v.x, v.y, v.z))

mesh.clear\_surfaces() mdt.commit\_to\_surface(mesh)
