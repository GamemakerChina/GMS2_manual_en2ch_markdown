# physics_particle_get_group_flags

With this function you can retrieve the group flags for a group of
particles. The group value is that which was returned when you created
the group of particles using the function [ physics_particle_group_end()
](physics_particle_group_end) , and the function will return a value
which is the combined value of the currently set flags.

#### Syntax:

``` gml
physics_particle_get_group_flags(group)
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
var flags = physics_particle_get_group_flags(group, flags);
if flags != (phy_particle_group_flag_solid | phy_particle_group_flag_rigid)
{
    flags = phy_particle_group_flag_solid | phy_particle_group_flag_rigid;
    physics_particle_set_group_flags(group, flags);
}
```

The above code will create a variable to store the flags value and then
use it to check the flags of the group indexed in the variable "group".
If they are not the same, the group is set with these flags.
