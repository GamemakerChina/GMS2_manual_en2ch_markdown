# part_particles_create_colour

This function is ideal for those effects that do not require any of the
functionality offered by [particle
emitters](../Particle_Emitters/Particle_Emitters) (for example, to
create smoke from a missile, or a simple explosion effect) as it permits
you to quickly and easily create particles at any position in the game
room. You can also colour the particles "on the fly" as they are created
with this function, and this colour will over-ride the predefined colour
of the particle, but it does not blend this colour over the particles
lifetime. Note that you must have created the particle system and the
particle type previously for this function to be used.

#### Syntax:

``` gml
part_particles_create_colour(ind, x, y, parttype, colour, number);
```

|          |                                                                                                                                      |                                                    |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                        |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system.                  |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The x coordinate of where to create the particles. |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The y coordinate of where to create the particles. |
| parttype |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)        | The index (type) of the particles to be created.   |
| colour   |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                          | The colour blending for the particles.             |
| number   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | The number of particles to create.                 |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (speed &amp;gt; 1)
{
    var _c = choose(c_aqua, c_lime, c_fuchsia, c_orange);
    part_particles_create_colour(sname, x, y, p_Smoke, _c, 1);
}
```

The above code will generate a single particle every step that the
instance with the code has a speed greater than one. These particles
will be of a random colour.
