# physics_particle_group_join

With this function you can join two particle groups together, and the
joined groups will then behave as if they were both part of a single
entity. The groups should have been created with over-lapping edges, as,
if they are not already touching, they will not be joined. The function
takes the unique group IDs of the groups to join, as returned by the
function [ physics_particle_group_end()
](physics_particle_group_end) , and you can use the function any
number of times for a single group to join various soft bodies together.

#### Syntax:

``` gml
physics_particle_group_join(to, from)
```

|          |                                                                                                                                           |                                    |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                                                                                      | Description                        |
| to       |  [Physics Particle Group ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_group_end)  | The first particle group to join.  |
| from     |  [Physics Particle Group ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_group_end)  | The second particle group to join. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var flags = phy_particle_flag_water | phy_particle_flag_viscous | phy_particle_flag_tensile;
var groupflags = phy_particle_group_flag_solid;
physics_particle_group_begin(flags, groupflags, mouse_x- 45, mouse_y, 0, 0, 0, 0, c_white, 1, 1, 2);
physics_particle_group_circle(50);
var g1 = physics_particle_group_end();
physics_particle_group_begin(flags, groupflags, mouse_x + 45, mouse_y, 0, 0, 0, 0, c_white, 1, 1, 2);
physics_particle_group_circle(50);
var g2 = physics_particle_group_end();
physics_particle_group_join(g1, g2);
```

The above code creates two circular particle groups and joins them
together.
