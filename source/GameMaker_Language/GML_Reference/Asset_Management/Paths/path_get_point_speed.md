# path_get_point_speed

With this function you can get the speed of the point (as defined in the
[Path Editor](../../../../The_Asset_Editors/Paths) or when you
dynamically add a path point using [ path_add_point()
](Path_Manipulation/path_add_point) ) expressed as a percentage. So,
if you have a path point set to 50 in the path editor, this function
would return 50 when used.

#### Syntax:

``` gml
path_get_point_speed(index, n);
```

|          |                                                                         |                                 |
|----------|-------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                    | Description                     |
| index    |  [Path Asset](../../../../../The_Asset_Editors/Paths)               | The index of the path to check. |
| n        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The point number to check.      |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (path_get_point_speed(pth_Patrol, 0) != 100)
{
    var _px = path_get_point_x(pth_Patrol, 0);
    var _py = path_get_point_x(pth_Patrol, 0);
    path_change_point(pth_Patrol, 0, _px, _py, 100);
}
```

The above code checks the path point "0" of the path indexed by
"pth_Patrol" to see if the speed is not equal to 100. If it is not then
it sets the speed of that point to 100.
