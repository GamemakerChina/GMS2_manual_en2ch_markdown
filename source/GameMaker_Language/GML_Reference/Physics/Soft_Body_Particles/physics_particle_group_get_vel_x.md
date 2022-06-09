# physics_particle_group_get_vel_x

With this function you can retrieve the horizontal velocity of a group
of particles. The group value is that which was returned when you
created the group of particles using the function [
physics_particle_group_end() ](physics_particle_group_end) , and the
function will return a value which is the combined value of the
currently set flags.

#### Syntax:

``` gml
physics_particle_group_get_vel_x(group)
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
vx = physics_particle_group_get_vel_x(group1); vy = physics_particle_group_get_vel_y(group1);
```

The above code will get the horizontal and vertical velocity of the
particle group indexed in the variable "group1" and store them in
variables.
