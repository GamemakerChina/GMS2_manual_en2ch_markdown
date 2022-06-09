# part_type_colour_mix

With this function you can set the given particle type to be a random
blend of two colours.

#### Syntax:

``` gml
part_type_colour_mix(ind, colour1, colour2);
```

|          |                                                                                                                                |                                             |
|----------|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                                                                           | Description                                 |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.   |
| colour1  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The first colour the blend will take from.  |
| colour2  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The second colour the blend will take from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_colour_mix(global.P_Damage, c_red, c_yellow);
```

The above code will set the colour for each particle emitted of the
particle type indexed in the global variable "P_Damage" to be a random
mix between the colours red and yellow.
