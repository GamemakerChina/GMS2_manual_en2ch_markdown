# physics_particle_group_end

This function is used to end the definition of a particle group shape.
Calling this function will create the particles within the given shape
parameters, and also return an ID value which can be stored and used in
further functions for interactions with the particle group.

#### Syntax:

``` gml
physics_particle_group_end()
```

#### Returns:

``` gml
 Physics Particle Group ID
```

#### Example:

``` gml
var flags = phy_particle_flag_water | phy_particle_flag_viscous | phy_particle_flag_tensile;
var groupflags = phy_particle_group_flag_solid;
physics_particle_group_begin(flags, groupflags, mouse_x, mouse_y, 0, 0, 0, 0, c_white, 1, 1, 2);
physics_particle_group_circle(100);
mLastGroup = physics_particle_group_end();
```

The above code stores the flags for the particle type and the particle
group properties in variables then uses these to create a circular
particle group with a 100px radius at the mouse position. The ID for the
group that has been created is stored in the variable "mLastGroup".
