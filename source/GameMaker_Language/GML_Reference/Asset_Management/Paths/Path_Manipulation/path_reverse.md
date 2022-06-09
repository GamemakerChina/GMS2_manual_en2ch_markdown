# path_reverse

With this function you can reverse the order in which the individual
path points are numbered, so, for example, if the path has 5 points,
point 0 would become point 4, point 1 would be point 3 and point 2 would
not be changed. The actual position of the points remains the same, only
the order in which they are processed is changed. **This function
changes the actual path asset** , and so will permanently affect how the
path is used by all instances in the game from the moment the function
is used until the end of the game. If this is not what you require, then
you should use a function like [path_duplicate()](path_duplicate) to
create a copy of the path first, then call this function on the
duplicated asset (don't forget to call [path_delete()](path_delete)
on the asset when it is no longer required).

#### Syntax:

``` gml
path_reverse(index);
```

|          |                                                               |                                  |
|----------|---------------------------------------------------------------|----------------------------------|
| Argument | Type                                                          | Description                      |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path to change. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_reverse(pth_AI);
```

This would reverse the order in which all points on the given path are
processed.
