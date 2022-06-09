# part_system_automatic_draw

This function can be used to switch off the drawing of a particle system
so that any updates done to the system (automatic or otherwise) will not
be seen. This is a purely visual option and when set to false you will
not be able to see the particles as they are not drawn, but they still
exists and are changing position, colour etc... as they would normally.
When automatic drawing is off, you can *explicitly* order GameMaker to
draw the current state of the particle system using the function [
part_system_drawit() ](part_system_drawit) , and if you set this
function to true again you can switch automatic drawing back on. One
thing to note is that if you are using the simple effects created by the
functions [ effect_create_above() ](../effect_create_above) or [
effect_create_below() ](../effect_create_below) then you can use the
values of 0 (for below effects) or 1 (for above effects) as the particle
system index and so toggle the automatic draw for these too (this will
also work to toggle drawing for the GML Visual particle effects).

#### Syntax:

``` gml
part_system_automatic_draw(ind, automatic);
```

|           |                                                                                                                                      |                                                        |
|-----------|--------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Argument  | Type                                                                                                                                 | Description                                            |
| ind       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to change.            |
| automatic |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                         | Whether automatic drawing is on (true) or not (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_system_automatic_draw(global.Sname, false);
```

The above code switches off automatic drawing for the particle system
indexed in the global variable "Sname".
