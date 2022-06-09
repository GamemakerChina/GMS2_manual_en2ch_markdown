# physics_particle_group_delete

With this function you can delete (remove) a particle group from the
physics simulation in the current room. The function takes the unique
group ID of the group to delete, as returned by the function [
physics_particle_group_end() ](physics_particle_group_end) .

#### Syntax:

``` gml
physics_particle_group_delete(ind)
```

|          |                                                                                                                                           |                                                 |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                                                                                      | Description                                     |
| ind      |  [Physics Particle Group ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_group_end)  | The index (ID) of the particle group to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_particle_group_delete(gp1);
```

The above code will delete all the particles that comprise the group
with the ID stored in the variable "gp1" from the simulation.
