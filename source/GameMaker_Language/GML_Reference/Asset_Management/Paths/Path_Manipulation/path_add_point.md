# path_add_point

With this function you can add a point to the specified path and set its
speed factor. This point is added onto the end of the path, irrespective
of the position of the point, and the factor is equal to the percentage
of [ path_speed ](../Path_Variables/path_speed) that the following
instance actually goes at when it reaches this point in the path. If you
wish to place a path point at some other position that is not the end,
you should use [ path_insert_point() ](path_insert_point) . If used
on a path from the Asset Browser, note that **the function will
change the actual asset** , and so will permanently affect how the path
is used by all instances in the game from the moment the function is
used until the end of the game. If this is not what you require, then
you should use a function like [path_duplicate()](path_duplicate) to
create a copy of the path first, then call this function on the
duplicated asset (don't forget to call [path_delete()](path_delete)
on the asset when it is no longer required).

#### Syntax:

``` gml
path_add_point(index, x, y, speed);
```

|          |                                                                            |                                                       |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                       | Description                                           |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to add the point to.            |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of the new point.                    |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of the new point.                    |
| speed    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The speed factor of the point (default value is 100). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
my_path = path_add();
for (var i = 0; i &amp;lt;= 360; i += 36;)
{
    path_add_point(my_path, x + lengthdir_x(50, i), y + lengthdir_y(50, i), 100);
}
```

The above code will create a circular path around the x/y position of
the instance running the code.
