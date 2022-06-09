# point_in_circle

When using this function, you define a circular area and GameMaker will
work out whether the given point falls within its bounds or not. If the
point falls within the defined circle the function will return true
otherwise the function will return false .

#### Syntax:

``` gml
point_in_circle(px, py, x1, y1, rad);
```

|          |                                                                         |                                         |
|----------|-------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                    | Description                             |
| px       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the point to check. |
| py       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the point to check. |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the circle centre.  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the circle centre.  |
| rad      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The radius of the circle.               |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if point_in_circle(mouse_x, mouse_y, x, y, 16)
{
    over = true;
}
else
{
    over = false;
}
```

The above code uses the point_in_circle function to check if the mouse
position falls within the defined circular area, setting the variable
"over" to true if it does, or false otherwise.
