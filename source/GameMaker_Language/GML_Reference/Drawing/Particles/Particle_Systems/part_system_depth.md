# part_system_depth

With this function you can set the draw depth for the particle system,
much the same as you can set the *render depth* of different layers
within the room, where a low draw depth means that it will appear on top
of all things drawn with a higher depth, and a high draw depth placing
it below everything with a lower draw depth.

#### Syntax:

``` gml
part_system_depth( ind, depth );
```

|          |                                                                                                                                      |                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                    |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to change.    |
| depth    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The depth at which to set the particle system. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
global.Sname = part_system_create();
part_system_depth(global.Sname, -1000 );
```

The above code will create a particle system and store its index in the
global variable "Sname". this system is then given a low depth of -1000,
meaning that it will appear above everything with a higher draw depth.
