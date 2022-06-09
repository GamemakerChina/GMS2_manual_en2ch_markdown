# path_add

With this function you can create a path in GameMaker without using the
path editor. This function will return the index of the path which
should be stored in a variable and used as the reference for that path
from then on. Please note that the created path is *empty* ie: it has no
points defined, so you will then have to use the [other available
functions](path_add_point) to add points to the path or be using [MP
grids](../../../Movement_And_Collisions/Motion_Planning/Motion_Planning)
to generate the path. Once you have finished using the path, or wish to
create a new one and store its index in the same variable you should
first delete the old path with [ path_delete ](path_delete) to
prevent memory leaks which can eventually crash your game.

#### Syntax:

``` gml
path_add();
```

#### Returns:

``` gml
 Path Asset
```

#### Example:

``` gml
global.newpath = path_add();
```

This will create a new path and assign its index to global.newpath.
