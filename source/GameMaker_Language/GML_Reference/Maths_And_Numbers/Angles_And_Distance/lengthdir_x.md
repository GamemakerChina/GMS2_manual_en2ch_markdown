# lengthdir_x

This function is used to get the **x** component of a position "len"
pixels from the starting point and in direction "dir". If you imagine a
circle around your instance, and then imagine a point anywhere on that
circle, to move to that point we need to move the object so many pixels
in that direction... so this function (when used with [ lengthdir_y()
](lengthdir_y) ) gets the position of that point on the circle to be
used in code by the instance. See the image below for details:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Maths/Lengthdir_Image.png)  

#### Syntax:

``` gml
lengthdir_x(len, dir);
```

|          |                                                                         |                                         |
|----------|-------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                    | Description                             |
| len      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The length away of the point to return. |
| dir      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The direction of the point to return.   |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _xx = x + lengthdir_x(64, image_angle); var _yy = y + lengthdir_y(64, image_angle); instance_create_layer(_xx, _yy, "Bullets", obj_bullet);
```

This will create a bullet instance at ( \_xx , \_yy ), which will be 64
pixels from the parent instance in the direction of the image angle.
