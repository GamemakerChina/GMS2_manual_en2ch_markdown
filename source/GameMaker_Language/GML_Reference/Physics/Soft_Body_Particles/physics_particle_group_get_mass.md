# physics_particle_group_get_mass

With this function you can retrieve the mass of an entire group of
particles. The group value is that which was returned when you created
the group of particles using the function [ physics_particle_group_end()
](physics_particle_group_end) .

#### Syntax:

``` gml
physics_particle_group_get_mass(group)
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
var _mass = physics_particle_group_get_mass(group1);
```

The above code will get the mass of the particle group indexed in the
variable "group1" and store it in a variable.
