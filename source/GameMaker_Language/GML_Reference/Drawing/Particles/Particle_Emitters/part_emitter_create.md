# part_emitter_create

This function must be used to create a new emitter and assign it to a
given particle system. The function will return the index value for the
new emitter which must be stored in a variable and used in all further
functions that reference the emitter, and the emitter itself must be
destroyed when no longer being used to prevent memory leaks (this can be
achieved using the specific emitter destroy functions or by destroying
the whole particle system that the emitter belongs to).

#### Syntax:

``` gml
part_emitter_create(ps);
```

|          |                                                                                                                                      |                                               |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                   |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The particle system to create the emitter in. |

#### Returns:

``` gml
 Particle Emitter ID
```

#### Example:

``` gml
p_emit1 = part_emitter_create(Sname);
```

This will create a new particle emitter and store its index in the
variable "p_emit".
