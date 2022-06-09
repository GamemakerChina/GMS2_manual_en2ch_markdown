# point_distance

This function returns the length of a vector formed by the specified
components \[x1,y1\] and \[x2,y2\]. For example, in the image below if
we want to get the distance between the player ship position and the
enemy position so that we can calculate if the enemy is close enough to
shoot at then we would use this function (the exact code is in the
example below the image):  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Maths/point_distance.png)  

#### **Syntax:**

``` gml
point_distance(x1, y1, x2, y2);
```

|          |                                                                         |                                                        |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                    | Description                                            |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the first component of the vector  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the first component of the vector  |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the second component of the vector |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the second component of the vector |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var ex, ey;
ex = instance_nearest(x, y, enemy).x;
ey = instance_nearest(x, y, enemy).y;
if (point_distance(x, y, ex, ey) &amp;lt; 200)
{
    instance_create_layer(x, y, "Bullets", obj_Missile)
}
```

The above code will get the x and y coordinates of the nearest enemy and
then use them to check the distance (length) of the vector formed by
them and the player coordinates. If the value is less than 200, the
player object will create an instance of "obj_Missile".
