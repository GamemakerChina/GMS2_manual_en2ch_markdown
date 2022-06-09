# part_type_colour3

This function can be used to set a three colour gradient for each
particle created of the given type. The first colour is that which all
particles will start with, and the second colour is the one that will be
blended to half way through its lifetime and the third colour is the one
with which the particle will end with. A smooth gradient change will
occur through the colours over the particles lifetime from one colour to
the other.

#### Syntax:

``` gml
part_type_colour3( ind, colour1, colour2, colour3 );
```

|          |                                                                                                                                |                                                               |
|----------|--------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                                           | Description                                                   |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.                     |
| colour1  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The colour the particle will start at.                        |
| colour2  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The colour the particle will be halfway through its lifespan. |
| colour3  |  [Colour](../../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                    | The colour the particle will end at.                          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_colour3( part_Health, c_red, c_white, c_maroon);
```

The above code will make all particles created of the type indexed in
the variable "part_Health" have a colour blend from red to white to
maroon over their lifetime.
