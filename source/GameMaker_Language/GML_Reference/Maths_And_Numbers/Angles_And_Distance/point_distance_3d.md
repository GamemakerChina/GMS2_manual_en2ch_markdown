# point_distance_3d

This function takes the supplied components of the vector and returns
the length (distance) of the vector. It works in exactly the same way as
[ point_distance() ](point_distance) but with the addition of
factoring in the z value (depth) for use in 3D space.

#### **Syntax:**

``` gml
point_distance_3d(x1, y1, z1, x2, y2, z2);
```

|          |                                                                         |                                                        |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                    | Description                                            |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the first component of the vector  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the first component of the vector  |
| z1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z coordinate of the first component of the vector  |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the second component of the vector |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the second component of the vector |
| z2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z coordinate of the second component of the vector |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var inst, ex, ey, ez;
inst = instance_nearest(x, y, enemy);
if inst
{
    ex = inst.x;
    ey = inst.y;
    ez = inst.z;
    if point_distance_3d(x, y, z, ex, ey, ez) &amp;lt; 200
    {
        instance_create_layer(x, y, "Bullets", obj_Missile)
    }
}
```

The above code will get the x and y and z coordinates of the nearest
enemy and then use them to check the distance (length) of the vector
formed by them and the player coordinates. If the value is less than
200, the player object will create an instance of "obj_Missile".
