# draw_clear

This function can be used to clear the entire screen (with no alpha
blend) to the given colour, and is only for use in the draw event of an
instance (it will not show if used in any other event). It can also be
useful for clearing [surfaces](../Surfaces/Surfaces) when they are
newly created.

#### Syntax:

``` gml
draw_clear(col);
```

|          |                                                                                                           |                                                  |
|----------|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                      | Description                                      |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  | The colour with which the screen will be cleared |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_clear(c_blue);
```

This will clear the screen with the colour blue.
