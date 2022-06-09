# angle_difference

This function will return the smallest difference between the two
specified angles, where the difference is calculated from the source
angle towards the destination angle. The returned value will be between
-180 and 180 degrees (where a positive angle is anti-clockwise and a
negative angle is clockwise). The relationship between the "source" and
"destination" angles is such that the difference that you get by calling
angle_difference(dest, src) , when added back to the src value, gives
you the dest angle (although the exact numeric values may differ). You
can use a similar technique to move the source angle towards the
destination angle gradually every step, where you add, say, 10% of the
returned difference back to src to move it a little bit towards dest
(this is demonstrated in the example below).

#### **Syntax:**

``` gml
angle_difference(dest, src)
```

|          |                                                                         |                                 |
|----------|-------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                    | Description                     |
| dest     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The destination or target angle |
| src      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The source angle                |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _dir = point_direction(x, y, mouse_x, mouse_y);
var _diff = angle_difference(_dir, image_angle);
image_angle += _diff * 0.1;
```

The above code will get the direction from the instance to the mouse
cursor, then get the difference between that angle and the current [
image_angle
](../../Asset_Management/Sprites/Sprite_Instance_Variables/image_angle)
, using this value to gradually rotate the instance towards the mouse.  
![](https://gms.magecorn.com/Manual/assets/Images/InteractiveExamples/DirectionalSprite.png)  

Interactive Example
