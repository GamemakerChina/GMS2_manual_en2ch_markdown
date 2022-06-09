# path_set_closed

This function can be used to flag a given path as being open (false) or
closed (true). A closed path has its start point connected to its end
point, forming a loop, and an open path has a definitive, unconnected
start and finish. **This function changes the actual path asset** , and
so will permanently affect how the path is used by all instances in the
game from the moment the function is used until the end of the game.If
this is not what you require, then you should use a function like
[path_duplicate()](path_duplicate) to create a copy of the path
first, then call this function on the duplicated asset (don't forget to
call [path_delete()](path_delete) on the asset when it is no longer
required).

#### Syntax:

``` gml
path_set_closed(index, closed);
```

|          |                                                                               |                                                   |
|----------|-------------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                          | Description                                       |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)                  | The index of the path to change.                  |
| closed   |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the path is closed (true) or not (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_set_closed(pth_Patrol, true);
```

This will set the given path to be a closed path.
