# path_clear_points

With this function you can remove all point definitions from a path,
effectively making an "empty" path. This *does not* delete the path, for
that you should use [ path_delete() ](path_delete) , however it
should be noted that **this function changes the actual path asset** ,
and so will permanently affect how the path is used by all instances in
the game from the moment the function is used until the end of the game.
If this is not what you require, then you should use a function like
[path_duplicate()](path_duplicate) to create a copy of the path
first, then call this function on the duplicated asset (don't forget to
call [path_delete()](path_delete) on the asset when it is no longer
required).

#### Syntax:

``` gml
path_clear_points(index);
```

|          |                                                               |                                 |
|----------|---------------------------------------------------------------|---------------------------------|
| Argument | Type                                                          | Description                     |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if path_get_number(mypath) &amp;gt; 0
{
    path_clear_points(mypath);
}
```

The above code checks to see if there are any points on the path indexed
in the variable "mypath" and if there are, it clears the path.
