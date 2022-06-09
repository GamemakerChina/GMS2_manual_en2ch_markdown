# part_type_colour2

This function can be used to set a two colour gradient for each particle
created of the given type. The first colour is that which all particles
will start with, and the second colour is the one on which the particle
will end with, and a smooth gradient change will occur to the colour
over the particles lifetime from one colour to the other.

#### Syntax:

``` gml
part_type_colour2(ind, colour1, colour2);
```

|          |                                                                                                                                |                                           |
|----------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                           | Description                               |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change. |
| colour1  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The colour the particle will start at.    |
| colour2  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The colour the particle will end at.      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_colour2( part_Health, c_red, c_white);
```

The above code will make all particles created of the type indexed in
the variable "part_Health" have a colour blend from red to white over
their lifetime.
