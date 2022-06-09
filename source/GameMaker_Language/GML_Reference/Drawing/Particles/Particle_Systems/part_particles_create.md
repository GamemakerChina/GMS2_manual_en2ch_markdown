# part_particles_create

This function is ideal for those effects that do not require any of the
functionality offered by [particle
emitters](../Particle_Emitters/Particle_Emitters) (for example, to
create smoke from a missile, or a simple explosion effect) as it permits
you to quickly and easily create particles at any position in the game
room. Note that you must have created the particle system and the
particle type previously for this function to be used.

#### Syntax:

``` gml
part_particles_create(ind, x, y, parttype, number);
```

|          |                                                                                                                                      |                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                        |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system.                  |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The x coordinate of where to create the particles. |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The y coordinate of where to create the particles. |
| parttype |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)        | The index (type) of the particles to be created.   |
| number   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The number of particles to create.                 |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button(mb_left)
{
    part_particles_create(sname, mouse_x, mouse_y, p_CursorEffect, 5);
}
```

The above code checks for the mouse button being pressed and if it
returns true it generates 5 particles at the mouse position.
