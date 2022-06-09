# point_direction

This function returns the direction of a vector formed by the specified
components \[x1,y1\] and \[x2,y2\] in relation to the fixed x/y
coordinates of the room. For example, in the image below if we want to
get the direction from the player ship position to the enemy position so
that we can fire a missile at the enemy then we would use this function
(the exact code is in the example below the image):  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Maths/point_direction.png)  

#### **Syntax:**

``` gml
point_direction(x1, y1, x2, y2)
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
with (instance_create_layer(x, y, "Bullets", obj_Missile))
{
    direction = point_direction(x, y, ex, ey);
}
```

The above code will get the x and y coordinates of the nearest enemy and
then pass them to a bullet object to use in the point_direction function
to set its direction of travel correctly.
