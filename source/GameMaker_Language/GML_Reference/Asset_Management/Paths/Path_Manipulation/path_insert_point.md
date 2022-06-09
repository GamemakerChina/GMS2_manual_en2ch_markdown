# path_insert_point

With this function you can insert a new point into a path (the path can
have been created in the path editor or through code using [ path_add()
](path_add) ). The point will be added into the path before the
point "n" that is specified in the function.

#### Syntax:

``` gml
path_insert_point(index, n, x, y, speed);
```

|          |                                                                            |                                                           |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                       | Description                                               |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to insert the point into.           |
| n        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The defining point to insert the new point BEFORE.        |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate (relative to the path) of the new point. |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate (relative to the path) of the new point. |
| speed    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The speed factor of the point.                            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_insert_point(mypath, 0, 50, 50, 100);
```

This will insert a point at the very beginning of the path indexed in
the variable "mypath", at (50,50), with a speed factor of 100%.
