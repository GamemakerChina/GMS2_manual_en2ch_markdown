# physics_particle_group_add_point

This function sets a point in the room to define the shape of a polygon
which will be used to create a group of soft body particles. You must
have previously signaled to GameMaker that you are going define a
polygon shape using the function
[physics_particle_group_polygon()](physics_particle_group_polygon)
and then use this function to define the individual points of the
polygon. You must give at least three points when defining the polygon
shape, but can give up to eight, and the function will permit the
definition of concave polygons. However, if you generate a polygon with
any cavities, the points within will be ignored and a convex shape will
be created for the particle group.

#### Syntax:

``` gml
physics_particle_group_add_point(x, y)
```

|          |                                                                         |                                           |
|----------|-------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                    | Description                               |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position in the room for the point. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position in the room for the point. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var flags = phy_particle_flag_water | phy_particle_flag_viscous | phy_particle_flag_tensile; var groupflags = phy_particle_group_flag_solid; physics_particle_group_begin(flags, groupflags, mouse_x, mouse_y, 0, 0, 0, 0, c_white, 1, 1, 2);physics_particle_group_polygon();
 physics_particle_group_add_point(200, 200); physics_particle_group_add_point(300, 300); physics_particle_group_add_point(100, 300); mLastGroup = physics_particle_group_end();
```

The above code stores the flags for the particle type and the particle
group properties in variables then uses these to create a polygon
particle group of three sides at the mouse position.
