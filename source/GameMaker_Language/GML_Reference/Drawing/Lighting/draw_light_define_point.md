# draw_light_define_point

This function is for defining a positional light, where you can define
the x, y and z position of the light, the light range and its colour
(which will also affect the perceived intensity of the light as certain
colours appear "darker" than others). You must also give the light an
index number which what will be used in other functions to reference it.
**NOTE** : There are only 8 hardware lights available, so only 8 defined
lights can be enabled at any one time (although more can be defined).

#### Syntax:

``` gml
draw_light_define_point(ind, x, y, z, range, col);
```

|          |                                                                                                           |                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Argument | Type                                                                                                      | Description                                                                 |
| ind      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The index number of the light (arbitrary)                                   |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The x position of the light                                                 |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The y position of the light                                                 |
| z        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The z position of the light                                                 |
| range    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The light range (in pixels)                                                 |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour to use for the light (either a constant, a real or a hex value). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_lighting(true); draw_light_define_point(1, 200, 123, 50, 2000, c_white); draw_light_enable(1, true);
```

The above code will enable lighting for the whole scene, then define a
white light at a specific point in the room space, and then finally turn
that light on.
