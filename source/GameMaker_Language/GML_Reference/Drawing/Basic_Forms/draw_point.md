# draw_point

With this function you can draw a single pixel anywhere on the screen,
using the currently set draw colour and alpha.

#### Syntax:

``` gml
draw_point(x, y);
```

|          |                                                                         |                                            |
|----------|-------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                    | Description                                |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the point to be drawn. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the point to be drawn. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_set_colour(c_yellow); draw_point(100,100);
```

This will draw a yellow pixel at position (100,100).
