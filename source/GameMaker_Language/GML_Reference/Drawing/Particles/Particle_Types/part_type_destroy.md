# part_type_destroy

With this function you can remove the specified particle type from the
game. When you use this function, all particles of the given type will
disappear from the room and the particle itself is removed form memory,
so this function should be used only when you no longer need the
particle.

#### Syntax:

``` gml
part_type_destroy(ind);
```

|          |                                                                                                                                |                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                                           | Description                                |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to destroy. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if part_particles_count(smoke_sys) = 0
{
    part_type_destroy(smoke_part);
    part_system_destroy(smoke_sys);
    instance_destroy();
}
else alarm[0] = 1;
```

The above code checks a particle system to see if any particles are
currently visible in the room and if not, the particles, the system and
the instance are destroyed.
