# motion_add

This function will modify the current
[direction](../../Asset_Management/Instances/Instance_Variables/direction)
and
[speed](../../Asset_Management/Instances/Instance_Variables/speed)
of the instance running the code, adding the new values to the current
values. If you wish to simply change these values, you should be using
the function [motion_set()](motion_set) .

#### Syntax:

``` gml
motion_add(dir, speed);
```

|          |                                                                         |                      |
|----------|-------------------------------------------------------------------------|----------------------|
| Argument | Type                                                                    | Description          |
| dir      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The added direction. |
| speed    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The added speed.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var pdir;
pdir = point_direction(other.x, other.y, x, y);
motion_add(pdir, other.speed);
if speed &amp;gt; 8 speed = 8;
```

the above code would be called in the collision event with another
object. It adds to the direction of motion and the speed of the instance
a vector based on the position and speed of the other instance involved
in the collision. It then limits the speed if it goes over 8 (pixels per
step).
