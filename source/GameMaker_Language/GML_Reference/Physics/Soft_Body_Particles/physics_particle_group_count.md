# physics_particle_group_count

This function will return the number of particles that are active in a
single group. The group index (ID) is the value that is returned when
you call the function [ physics_particle_group_end()
](physics_particle_group_end) .

#### Syntax:

``` gml
physics_particle_group_count(group)
```

|          |                                                                                                                                           |                                                      |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                                                                                      | Description                                          |
| group    |  [Physics Particle Group ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_group_end)  | The group index (ID) of the particle group to count. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
gp_num = physics_particle_group_count(group1);
```

The above code will get the number of particles used to make the group
indexed in the variable "group1" and store the value in a variable.
