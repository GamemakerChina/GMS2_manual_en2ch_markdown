# part_particles_count

With this function you can check to see if a particle system currently
has any particles created in the room, and it will return the number of
them too.

#### Syntax:

``` gml
part_particles_count(ind);
```

|          |                                                                                                                                      |                                   |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                                                 | Description                       |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (part_particles_count(Sname) == 0)
{
    part_system_destroy(Sname);
    instance_destroy();
}
```

The above code will check the number of particles in the local particle
system indexed in the variable "Sname" and if there are none, it will
destroy the system and then the instance.
