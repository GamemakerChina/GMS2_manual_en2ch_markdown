# point_in_triangle

When using this function, you define a triangular area and GameMaker
will work out whether the given point falls within its bounds or not. If
the point falls within the defined triangle the function will return
true otherwise the function will return false .

#### Syntax:

``` gml
point_in_triangle(px, py, x1, y1, x2, y2, x3, y3);
```

|          |                                                                         |                                                                 |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                     |
| px       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the point to check.                         |
| py       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the point to check.                         |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the first corner of the triangle to check.  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the first corner of the triangle to check.  |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the second corner of the triangle to check. |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the second corner of the triangle to check. |
| x3       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the third corner of the triangle to check.  |
| y3       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the third corner of the triangle to check.  |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var inst = instance_nearest(x, y, obj_Player);
if instance_exists(inst)
{
    var x1 = x + lengthdir_x(100, image_angle - 45);
    var y1 = y + lengthdir_y(100, image_angle - 45);
    var x2 = x + lengthdir_x(100, image_angle + 45);
    var y2 = y + lengthdir_y(100, image_angle + 45);
    if point_in_triangle(inst.x, inst.y, x, y, x1, y1, x2, y2)
    {
        can_see = true;
    }
}
```

The above code uses the point_in_triangle function as a "cone of vision"
to check for an instance of "obj_player", setting a variable to true
should the objects x/y position fall within the defined triangle.
