# draw_light_define_ambient

This function is used to control the ambient light of a scene, which is
the light that you have in a scene even without having defined any point
or directional light sources. It is effectively the overall colour and
brightness (or darkness) of a scene. The default colour is c_black .

#### Syntax:

``` gml
draw_light_define_ambient(col);
```

|          |                                                                                                           |                                                               |
|----------|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                   |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to use (either a constant, a real or a hex value). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_light_define_ambient(c_white);
```

The above code will define the ambient lighting as being white.
