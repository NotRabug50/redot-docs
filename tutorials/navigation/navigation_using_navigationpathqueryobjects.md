# Using NavigationPathQueryObjects

`NavigationPathQueryObjects` can be used together with
`NavigationServer.query_path()` to obtain a heavily **customized**
navigation path including optional **meta data** about the path.

This requires more setup compared to obtaining a normal NavigationPath
but lets you tailor the pathfinding and provided path data to the
different needs of a project.

NavigationPathQueryObjects consist of a pair of objects, a
`NavigationPathQueryParameters` object holding the customization options
for the query and a `NavigationPathQueryResult` that receives (regular)
updates with the resulting path and meta data from the query.

2D and 3D versions of `NavigationPathQueryParameters` are available as
`NavigationPathQueryParameters2D<class_NavigationPathQueryParameters2D>`
and
`NavigationPathQueryParameters3D<class_NavigationPathQueryParameters3D>`
respectively.

2D and 3D versions of `NavigationPathQueryResult` are available as
`NavigationPathQueryResult2D<class_NavigationPathQueryResult2D>` and
`NavigationPathQueryResult3D<class_NavigationPathQueryResult3D>`
respectively.

Both parameters and result are used as a pair with the
`NavigationServer.query_path()` function.

For the available customization options and their use see the class doc
of the parameters.

While not a strict requirement, both objects are intended to be created
once in advance, stored in a persistent variable for the agent and
reused for every followup path query with updated parameters. This reuse
avoids performance implications from frequent object creation if a
project has a large quantity of simultaneous agents that regularly
update their paths.

.. code-tab:: gdscript 2D GDScript

\# Prepare query objects. var query\_parameters :=
NavigationPathQueryParameters2D.new() var query\_result :=
NavigationPathQueryResult2D.new()

func query\_path(p\_start\_position: Vector2, p\_target\_position: Vector2, p\_navigation\_layers: int = 1) -&gt; PackedVector2Array:  
if not is\_inside\_tree():  
return PackedVector2Array()

query\_parameters.map = get\_world\_2d().get\_navigation\_map()
query\_parameters.start\_position = p\_start\_position
query\_parameters.target\_position = p\_target\_position
query\_parameters.navigation\_layers = p\_navigation\_layers

NavigationServer2D.query\_path(query\_parameters, query\_result) var
path: PackedVector2Array = query\_result.get\_path()

return path

gdscript 3D GDScript

\# Prepare query objects. var query\_parameters :=
NavigationPathQueryParameters3D.new() var query\_result :=
NavigationPathQueryResult3D.new()

func query\_path(p\_start\_position: Vector3, p\_target\_position: Vector3, p\_navigation\_layers: int = 1) -&gt; PackedVector3Array:  
if not is\_inside\_tree():  
return PackedVector3Array()

query\_parameters.map = get\_world\_3d().get\_navigation\_map()
query\_parameters.start\_position = p\_start\_position
query\_parameters.target\_position = p\_target\_position
query\_parameters.navigation\_layers = p\_navigation\_layers

NavigationServer3D.query\_path(query\_parameters, query\_result) var
path: PackedVector3Array = query\_result.get\_path()

return path
