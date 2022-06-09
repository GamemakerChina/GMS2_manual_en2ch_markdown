# part_system_update

With this function you can force a particle system to draw all the
current particles on the screen. If [ part_system_automatic_draw()
](part_system_automatic_draw) is switched off then this function
will show the particles when used in the draw event of an instance, or
it can be used when the drawing target is set to a surface (using [
surface_set_target() ](../../Surfaces/surface_set_target) ) to draw
the particles in the system to that surface.

#### Syntax:

``` gml
part_system_drawit(ind);
```

|          |                                                                                                                                      |                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                                |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to draw the particles of. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if surface_exists(surf)
{
    surface_set_target(surf);
    part_system_drawit(global.psys);
    surface_reset_target();
}
```

The above code checks to see if the surface indexed in the variable
"surf" exists, and if it does it then sets the drawing target to the
surface, draws the particle system with the ID stored in the global
variable, and then resets the drawing target so all normal drawing
appears on the screen once more.
