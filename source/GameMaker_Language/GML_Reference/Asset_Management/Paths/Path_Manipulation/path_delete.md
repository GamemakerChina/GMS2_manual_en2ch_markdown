# path_delete

You can use this code to remove a path from memory. If this path has
been created dynamically using [ path_add() ](path_add) , the
variable that holds the path index will no longer be valid for accessing
the path as it no longer exists, and if the path was created using the
[Path Editor](../../../../../The_Asset_Editors/Paths) that path can
no longer be accessed in the *whole game* as you are permanently
deleting it.

#### Syntax:

``` gml
path_delete(index);
```

|          |                                                               |                                  |
|----------|---------------------------------------------------------------|----------------------------------|
| Argument | Type                                                          | Description                      |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var t_path = path_add();
if mp_grid_path(grid, t_path, x, y, obj_Player.x, obj_Player.y, 1)
{
    path_assign(mypath, t_path);
}
path_delete(t_path);
```

The above code will create a path and store its index in a local
variable. This path is then used to store an [ mp_grid_path()
](../../../Movement_And_Collisions/Motion_Planning/mp_grid_path)
generated path which, if it succeeds in finding its way to the target,
is then assigned to the path indexed in "mypath". Finally the "t_path"
is deleted.
