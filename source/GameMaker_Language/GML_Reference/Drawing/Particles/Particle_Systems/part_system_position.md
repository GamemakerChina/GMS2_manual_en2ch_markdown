# part_system_position

With this function you can set the base position for the particle system
relative to the (0,0) position of the room, meaning that all further
particle functions relating to this system will now be drawn relative to
the new position. By default this position is always (0,0), but in some
very special circumstances you may wish to change this to something
else. **NOTE** : This function will change **everything** within the
particle system, so if you have an emitter at position (100,100) and
then set the particle system position to (0,100), the emitter will now
draw at (100,200). The same goes if you shift the system and then create
the emitter, as even though you create it at (100,100) it will be drawn
at (100,200).

#### Syntax:

``` gml
part_system_position(ind, x, y);
```

|          |                                                                                                                                      |                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                  |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to change.  |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The new x coordinate of the particle system. |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The new y coordinate of the particle system. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    part_system_position(global.Sname, mouse_x, mouse_y);
}
```

The above code will check for the press of the mouse button and if it
detects one, the particle system indexed in the global variable "Sname"
is shifted to the mouse x/y position
