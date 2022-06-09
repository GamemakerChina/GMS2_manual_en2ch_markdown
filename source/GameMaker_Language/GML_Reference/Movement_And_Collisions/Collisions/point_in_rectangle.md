# point_in_rectangle

When using this function, you define a rectangular area and GameMaker
will work out whether the given point falls within its bounds or not. If
the point falls within the defined rectangle the function will return
true otherwise the function will return false .

#### Syntax:

``` gml
point_in_rectangle(px, py, x1, y1, x2, y2);
```

|          |                                                                         |                                                                |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                    |
| px       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the point to check.                        |
| py       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the point to check.                        |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the left side of the rectangle to check.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the top side of the rectangle to check.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the right side of the rectangle to check.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the bottom side of the rectangle to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if point_in_rectangle(mouse_x, mouse_y, x -10, y - 10, x + 10, y + 10)
{
    audio_play_sound(snd_click, 0, false);
}
```

This short code checks the mouse position against the defined
rectangular area and plays a sound if it falls within the bounds.
