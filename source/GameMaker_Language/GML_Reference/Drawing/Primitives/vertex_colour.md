# vertex_colour

If your defined vertex format takes a colour value you can use this
function to add that data to the vertex being defined for the current
primitive. The function needs a buffer to store the data in and will
take either a [colour
constant](../Colour_And_Alpha/Colour_And_Alpha) , or a hex value
(using the standard GameMaker format of BGR, eg: $FF0000 for blue) as
well as an alpha value from 0 (transparent) to 1 (fully opaque).

#### Syntax:

``` gml
vertex_colour(buffer, colour, alpha);
```

|          |                                                                                                                   |                                                                |
|----------|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                                                              | Description                                                    |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to.                        |
| colour   |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)          | The colour for this vertex (can be a constant or a hex value). |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                            | The alpha value for the vertex (from 0 to 1).                  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_colour(b, c_white, 1);
```

The above code will set the vertex being defined to be white with an
alpha value of 1.
