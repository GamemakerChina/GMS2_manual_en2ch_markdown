# physics_particle_delete

With this function you can delete (remove) a particle from the physics
simulation in the current room. The function takes the unique ID of the
particle to delete, as returned by the function [
physics_particle_create() ](physics_particle_create) .

#### Syntax:

``` gml
physics_particle_group_delete(ind)
```

|          |                                                                                                                                  |                                           |
|----------|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                             | Description                               |
| ind      |  [Physics Particle ID](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_create)  | The index (ID) of the particle to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_particle_delete(part);
```

The above code will delete the particle with the ID stored in the
variable "part" from the simulation.
