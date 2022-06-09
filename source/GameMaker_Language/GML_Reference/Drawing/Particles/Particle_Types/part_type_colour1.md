# part_type_colour1

This function is used to set a particle type to be a single colour for
the total duration of the lifetime of each individual particle.

#### Syntax:

``` gml
part_type_colour1(ind, colour1);
```

|          |                                                                                                                                |                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                           | Description                                  |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.    |
| colour1  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The single colour to make the particle type. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_colour1(global.Snow_Part, c_white);
```

The above code will set all particles created of the particle type
indexed in the global variable "Snow_Part" to be white only.
