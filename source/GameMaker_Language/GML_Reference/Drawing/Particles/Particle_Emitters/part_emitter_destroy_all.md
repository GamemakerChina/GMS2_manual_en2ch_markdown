# part_emitter_destroy_all

This function will remove all defined emitters from the given system and
clear them from memory (this will also stop any particles from being
produced by the given emitter, but it does *NOT* remove them from the
room). This function should always be called when the emitters are no
longer needed for the system to prevent memory leaks and errors.

#### Syntax:

``` gml
part_emitter_destroy_all( ps );
```

|          |                                                                                                                                      |                                                   |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                       |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The particle system to destroy all emitters from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if lives == 0
{
    part_emitter_destroy_all(global.Sname);
    room_goto(rm_Menu);
}
```

The above code checks the built in global variable "lives" and if it is
0, it destroys all particle emitters and then changes room.
