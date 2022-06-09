# path_get_y

With this function you can get the y coordinate of a position on any
given path. 0 is the start of the path, 1 is the end of the path, and
anything in between equates to the normalised distance along the length
of the path. This value needn't be a defining point of the path, it can
be anywhere on it.

#### Syntax:

``` gml
path_get_y(ind, pos);
```

|          |                                                                         |                                                                   |
|----------|-------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                       |
| index    |  [Path Asset](../../../../../The_Asset_Editors/Paths)               | The index of the path to check.                                   |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | How far through the path to check. Between 0 (start) and 1 (end). |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
y = path_get_y(pth_WallWalk, 0.5);
```

This will set the calling instance's y to the y coordinate of the point
at exactly halfway through the given path.
