# path_assign

With this function you can copy the path data from one path to another.
The path being copied *to* will be cleared first (should it have any
path points) and be **completely overwritten** by the path being copied
from. Neither path is deleted in the process and the result is two
paths, with two different indexes, but the exact same form and points.
In general you would want to use this function on a path created using
[path_add()](path_add) , since if you use it on a path asset, **it
will permanently affect the path for all instances in the game** from
the moment the function is used until the end of the game.

#### Syntax:

``` gml
path_assign(index, path);
```

|          |                                                               |                                                    |
|----------|---------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                          | Description                                        |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path to be overwritten.           |
| path     |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path that will overwrite 'index'. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
mypath = path_add(); path_assign(mypath, choose(path_1, path_2, path_3));
```

The above code will create a new, empty path indexed in the variable
"mypath" and then copy over the path data from one of the three
available path resources.
