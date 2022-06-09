# physics_particle_group_get_ang_vel

With this function you can retrieve the angular velocity of a group of
particles. The group value is that which was returned when you created
the group of particles using the function [ physics_particle_group_end()
](physics_particle_group_end) , and the function will return a value
which is the combined value of the currently set flags.

#### Syntax:

``` gml
physics_particle_group_get_ang_vel(group)
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
ang_v = physics_particle_group_get_ang_vel(group1);
```

The above code will get the angular velocity of the particle group
indexed in the variable "group1" and store it in a variable.
