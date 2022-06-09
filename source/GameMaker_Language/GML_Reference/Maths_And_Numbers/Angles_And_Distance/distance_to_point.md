# distance_to_point

This function calculates the distance from the edge of the bounding box
of the calling instance to the specified x/y position in the room, with
the return value being in pixels. Note that if the calling object have
no sprite or no mask defined, the results will be incorrect.

#### **Syntax:**

``` gml
distance_to_point(x, y);
```

|          |                                                                         |                          |
|----------|-------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                    | Description              |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position to check. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (distance_to_point(obj_Player.x, obj_Player.y) &amp;lt; range)
{
    canshoot = true;
}
```

The above code will check for the distance to the player object x/y
position and if it is less than the value stored in the variable "range"
the variable "canshoot" is set to true.
