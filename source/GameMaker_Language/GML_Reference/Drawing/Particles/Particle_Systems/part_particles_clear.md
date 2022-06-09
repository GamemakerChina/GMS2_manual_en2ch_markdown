# part_particles_clear

With this function you can clear all the particles currently created by
the system from the room. It does *not* reset or remove the particle
types themselves, just their visual representation, and if you have any
object streaming particles from an emitter, these particles disappear
but will begin to appear again the next step after calling this code.

#### Syntax:

``` gml
part_particles_clear(ind);
```

|          |                                                                                                                                      |                                   |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                                                 | Description                       |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (lives &amp;lt;= 0)
{
    part_particles_clear(global.Sname);
    room_goto(rm_intro);
}
```

The above code will check the value of the variable "lives" and if it is
equal to 0, it clears all particles from the system and then changes
room.
