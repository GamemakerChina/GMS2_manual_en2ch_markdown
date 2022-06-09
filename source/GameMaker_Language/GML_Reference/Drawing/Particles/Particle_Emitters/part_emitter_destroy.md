# part_emitter_destroy

This function will remove the specified emitter from the given system
and clear it from memory (this will also stop any particles from being
produced by the given emitter, but it does *NOT* remove them from the
room). This function should always be called when the given emitter is
no longer needed for the system to prevent memory leaks and errors.

#### Syntax:

``` gml
part_emitter_destroy( ps, ind );
```

|          |                                                                                                                                         |                                                  |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                                    | Description                                      |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)     | The particle system to destroy the emitter from. |
| ind      |  [Particle Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_create)  | The index of the emitter to destroy.             |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if part_emitter_exists(global.Sname, p_emit)
{
    part_emitter_destroy(global.Sname, p_emit1);
}
```

The above code will check to see if the particle emitter indexed in the
variable "p_emit" exists in the give particle system and if it does it
is destroyed.
