# path_change_point

With this function you can change the position and/or the speed factor
of any point previously defined for a path (the path can have been
created in the path editor or through code using [ path_add()
](path_add) ). If used on a path from the Asset Browser, note that
**the function will change the actual asset** , and so will permanently
affect how the path is used by all instances in the game from the moment
the function is used until the end of the game. If this is not what you
require, then you should use a function like
[path_duplicate()](path_duplicate) to create a copy of the path
first, then call this function on the duplicated asset (don't forget to
call [path_delete()](path_delete) on the asset when it is no longer
required).

#### Syntax:

``` gml
path_change_point(index, n, x, y, speed);
```

|          |                                                                            |                                                           |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                       | Description                                               |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to change a point of.               |
| n        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The defining point to change the attributes of.           |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new x coordinate (relative to the path) of the point. |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new y coordinate (relative to the path) of the point. |
| speed    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new speed factor of the point.                        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; path_get_number(path0); ++i;)
{
    var px = path_get_point_x(pth_Patrol, i) + 64 - random(128);
    var py = path_get_point_y(pth_Patrol, i) + 64 - random(128);
    path_change_point(pth_Patrol, i, px, py, 100);
}
```

The above code loops through all the points in the path indexed as
"path0" and re-positions all the points to a random position within an
area of 128x128 pixels.
