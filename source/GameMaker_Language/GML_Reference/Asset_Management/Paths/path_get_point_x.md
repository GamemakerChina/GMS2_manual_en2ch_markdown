# path_get_point_x

This function will return the x position (in room coordinates) of the
point that you input for the path that you index. If the point is
outside of the range of the path (ie: a path has 8 points and you ask
for the x position of point 10) then a value of 0 will be returned.

#### Syntax:

``` gml
path_get_point_x(index, n);
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
if (path_position == 1)
{
    var _num = path_get_number(pth_Patrol);
    var _pos = floor(random(_num));
    x = path_get_point_x(pth_Patrol, _pos);
    y = path_get_point_y(pth_Patrol, _pos);
    path_position = (1 / _num) * _pos;
}
```

The above code will check to see if an instance is at the end of a path.
If it is it will then choose a random point on the path and move the
instance to that point.
