# path_append

With this code you can append one path onto another one, effectively
joining them together, and for this to work, both paths must previously
exist. In general you would want to use this function on paths created
using [path_add()](path_add) , since if you use it on a path asset,
**it will permanently affect the path for instances in the game** from
the moment the function is used until the end of the game. NOTE This
will not remove the path being appended from the game. It is still
there, only it now has no points in it and if you no longer wish to use
it you should remove it with the function [ path_delete()
](path_delete) .

#### Syntax:

``` gml
path_append(index, path);
```

|          |                                                               |                                                         |
|----------|---------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                          | Description                                             |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The new index of the path.                              |
| path     |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path that will be appended to 'index'. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_append(mypath, mppath);
path_delete(mppath);
```

The above code appends the path data indexed in the variable "mppath" to
the path indexed in the variable "mypath" and then deletes the "mppath"
from memory.
