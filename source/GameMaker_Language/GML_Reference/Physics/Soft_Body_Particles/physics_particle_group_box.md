# physics_particle_group_box

This function will set the shape of the particle group that is being
created. You must first have begun the group definition using the
function [ physics_particle_group_begin()
](physics_particle_group_begin) , and then you would use this
function to set the approximate half width and half height of the group
in pixels - approximate because the exact width and height will depend
on the size of the base particles, as defined by the [
physics_particle_set_radius() ](physics_particle_set_radius)
function, as the physics simulation tries to "fit" as many of the
particles as possible into the defined shape. Finally you need to call [
physics_particle_group_end() ](physics_particle_group_end) to create
the group of particles in the room.

#### Syntax:

``` gml
physics_particle_group_box(halfWidth, halfHeight)
```

|            |                                                                         |                               |
|------------|-------------------------------------------------------------------------|-------------------------------|
| Argument   | Type                                                                    | Description                   |
| halfWidth  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The *half* width of the box.  |
| halfHeight |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The *half* height of the box. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var flags = phy_particle_flag_water | phy_particle_flag_viscous | phy_particle_flag_tensile;
var groupflags = phy_particle_group_flag_solid;
physics_particle_group_begin(flags, groupflags, mouse_x, mouse_y, 0, 0, 0, 0, c_white, 1, 1, 2);
physics_particle_group_box(100, 100);
mLastGroup = physics_particle_group_end();
```

The above code stores the flags for the particle type and the particle
group properties in variables then uses these to create a rectangular
particle group with sides of 200px at the mouse position.
