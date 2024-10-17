github\_url  
hide

# LightmapProbe

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Represents a single manually placed probe for dynamic object lighting
with `LightmapGI<class_LightmapGI>`.

classref-introduction-group

## Description

**LightmapProbe** represents the position of a single manually placed
probe for dynamic object lighting with `LightmapGI<class_LightmapGI>`.
Lightmap probes affect the lighting of
`GeometryInstance3D<class_GeometryInstance3D>`-derived nodes that have
their
`GeometryInstance3D.gi_mode<class_GeometryInstance3D_property_gi_mode>`
set to
`GeometryInstance3D.GI_MODE_DYNAMIC<class_GeometryInstance3D_constant_GI_MODE_DYNAMIC>`.

Typically, `LightmapGI<class_LightmapGI>` probes are placed
automatically by setting
`LightmapGI.generate_probes_subdiv<class_LightmapGI_property_generate_probes_subdiv>`
to a value other than
`LightmapGI.GENERATE_PROBES_DISABLED<class_LightmapGI_constant_GENERATE_PROBES_DISABLED>`.
By creating **LightmapProbe** nodes before baking lightmaps, you can add
more probes in specific areas for greater detail, or disable automatic
generation and rely only on manually placed probes instead.

\*\*Note:\*\* **LightmapProbe** nodes that are placed after baking
lightmaps are ignored by dynamic objects. You must bake lightmaps again
after creating or modifying **LightmapProbe**s for the probes to be
effective.
