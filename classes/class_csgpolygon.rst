.. Generated automatically by doc/tools/makerst.py in Godot's source tree.
.. DO NOT EDIT THIS FILE, but the CSGPolygon.xml source instead.
.. The source is found in doc/classes or modules/<name>/doc_classes.

.. _class_CSGPolygon:

CSGPolygon
==========

**Inherits:** :ref:`CSGPrimitive<class_csgprimitive>` **<** :ref:`CSGShape<class_csgshape>` **<** :ref:`VisualInstance<class_visualinstance>` **<** :ref:`Spatial<class_spatial>` **<** :ref:`Node<class_node>` **<** :ref:`Object<class_object>`

**Category:** Core

Brief Description
-----------------

Extrudes a 2D polygon shape to create a 3D mesh.

Member Variables
----------------

  .. _class_CSGPolygon_depth:

- :ref:`float<class_float>` **depth** - Extrusion depth when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_DEPTH.

  .. _class_CSGPolygon_material:

- :ref:`Material<class_material>` **material** - Material to use for the resulting mesh.

  .. _class_CSGPolygon_mode:

- :ref:`Mode<enum_csgpolygon_mode>` **mode** - Extrusion mode.

  .. _class_CSGPolygon_path_continuous_u:

- :ref:`bool<class_bool>` **path_continuous_u** - If true the u component of our uv will continuously increase in unison with the distance traveled along our path when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_interval:

- :ref:`float<class_float>` **path_interval** - Interval at which a new extrusion slice is added along the path when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_joined:

- :ref:`bool<class_bool>` **path_joined** - If true the start and end of our path are joined together ensuring there is no seam when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_local:

- :ref:`bool<class_bool>` **path_local** - If false we extrude centered on our path, if true we extrude in relation to the position of our CSGPolygon when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_node:

- :ref:`NodePath<class_nodepath>` **path_node** - The :ref:`Shape<class_shape>` object containing the path along which we extrude when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_path_rotation:

- :ref:`PathRotation<enum_csgpolygon_pathrotation>` **path_rotation** - The method by which each slice is rotated along the path when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_PATH.

  .. _class_CSGPolygon_polygon:

- :ref:`PoolVector2Array<class_poolvector2array>` **polygon** - Point array that defines the shape that we'll extrude.

  .. _class_CSGPolygon_smooth_faces:

- :ref:`bool<class_bool>` **smooth_faces** - Generates smooth normals so smooth shading is applied to our mesh.

  .. _class_CSGPolygon_spin_degrees:

- :ref:`float<class_float>` **spin_degrees** - Degrees to rotate our extrusion for each slice when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_SPIN.

  .. _class_CSGPolygon_spin_sides:

- :ref:`int<class_int>` **spin_sides** - Number of extrusion when :ref:`mode<class_CSGPolygon_mode>` is constant MODE_SPIN.


Enums
-----

  .. _enum_CSGPolygon_Mode:

enum **Mode**

- **MODE_DEPTH** = **0** --- Shape is extruded to :ref:`depth<class_CSGPolygon_depth>`.
- **MODE_SPIN** = **1** --- Shape is extruded by rotating it around an axis.
- **MODE_PATH** = **2** --- Shape is extruded along a path set by a :ref:`Shape<class_shape>` set in :ref:`path_node<class_CSGPolygon_path_node>`.

  .. _enum_CSGPolygon_PathRotation:

enum **PathRotation**

- **PATH_ROTATION_POLYGON** = **0** --- Slice is not rotated.
- **PATH_ROTATION_PATH** = **1** --- Slice is rotated around the up vector of the path.
- **PATH_ROTATION_PATH_FOLLOW** = **2** --- Slice is rotate to match the path exactly.


Description
-----------

This node takes a 2D polygon shape and extrudes it to create a 3D mesh.

