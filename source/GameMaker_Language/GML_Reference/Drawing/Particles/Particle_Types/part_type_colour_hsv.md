# part_type_colour_hsv

With this function you can set a hue, saturation and value range for all
particles of the given type. You supply a minimum value and a maximum
value for each of the three components and the particles created will
have a random colour based on the given range of parameters. In this way
you can create particles of the same hue but different saturations, or
of different hues but the same value (luminosity) etc... All values must
be between 0 and 255.

#### Syntax:

``` gml
part_type_colour_hsv(ind, hmin, hmax, smin, smax, vmin, vmax);
```

|          |                                                                                                                                |                                                             |
|----------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                                                                           | Description                                                 |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.                   |
| hmin     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum the final colour's hue component can be.        |
| hmax     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum the final colour's hue component can be.        |
| smin     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum the final colour's saturation component can be. |
| smax     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum the final colour's saturation component can be. |
| vmin     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum the final colour's value component can be.      |
| vmax     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum the final colour's value component can be.      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_hsv(global.Stars, 0, 255, 0, 255, 255, 255 );
```

The above code sets each particle emitted of the particle type indexed
in the global variable "Stars" to have different colours and
saturations, but the same value (luminosity).
