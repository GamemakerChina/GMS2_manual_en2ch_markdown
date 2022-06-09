# physics_particle_group_get_centre_y

With this function you can retrieve the y component of the center of
mass of an entire group of particles. The group value is that which was
returned when you created the group of particles using the function [
physics_particle_group_end() ](physics_particle_group_end) , and the
function will return a value which is the combined value of the
currently set flags.

#### Syntax:

``` gml
physics_particle_group_get_centre_y(group)
```

|          |                                                                                                                                           |                            |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                                                      | Description                |
| group    |  [Physics Particle Group ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_group_end)  | The particle group to get. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
xx = physics_particle_group_get_centre_x(group1); yy = physics_particle_group_get_centre_y(group1);
```

The above code will get the x and y position for the center of mass of
the particle group indexed in the variable "group1" and store them in
variables.
