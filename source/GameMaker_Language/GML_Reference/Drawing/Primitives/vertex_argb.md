# vertex_argb

This function will set the ARGB values for the vertex currently being
defined for the custom primitive. You supply the buffer to write the
data into as well as the red, green, blue and alpha values that you wish
to use as a single 32-bit unsigned integer - alpha sample in the highest
8 bits, followed by the red sample, green sample and finally the blue
sample in the lowest 8 bits. You can use hex notation ($AARRGGBB) a real
number or use any of the make_colour\_\*() functions to define the
colour value.

#### Syntax:

``` gml
vertex_argb(buffer, argb);
```

|          |                                                                                                                   |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                              | Description                             |
| buffer   |  [Vertex Buffer ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/vertex_create_buffer)  | The buffer to write the information to. |
| argb     |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)          | The ARGB value to set.                  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
vertex_argb(buff, $FFFFFFFF);
```

The above code will set the ARGB values of the vertex being defined to
white.
