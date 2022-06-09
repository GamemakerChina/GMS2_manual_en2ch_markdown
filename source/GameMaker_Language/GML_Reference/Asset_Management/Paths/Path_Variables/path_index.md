# path_index

All resources in GameMaker have a unique identifying number, and the
path_index is a **read-only** variable that holds the index value for a
given path asset that has been assigned to an instance using the
[path_start()](../path_start) function. If the instance has no path
assigned, the variable will be set to -1.

#### Syntax:

``` gml
path_index;
```

#### Returns:

``` gml
 Path Asset
```

#### Example:

``` gml
if (path_index == -1)
{
    path_start(pth_enemy3, 4, path_action_reverse, 0);
}
```

The above code checks to see if a path has been assigned to the
instance, and if not it starts a new path (assigning it to the
path_index at the same time).
