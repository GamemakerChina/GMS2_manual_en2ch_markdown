# path_rescale

This function can be used to re-scale the given path along both (or
either) the vertical and horizontal axis, basically moving each of the
path points to a new position corresponding to this scale around the
centre of the path. **This function changes the actual path asset** ,
and so will permanently affect how the path is used by all instances in
the game from the moment the function is used until the end of the
game. If this is not what you require, then you should use a function
like [path_duplicate()](path_duplicate) to create a copy of the path
first, then call this function on the duplicated asset (don't forget to
call [path_delete()](path_delete) on the asset when it is no longer
required).

#### Syntax:

``` gml
path_rescale(index, xscale, yscale);
```

|          |                                                                            |                                                                       |
|----------|----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                           |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to scale.                                       |
| xscale   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | What to multiply the current horizontal scale by. Default scale is 1. |
| yscale   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | What to multiply the current vertical scale by. Default scale is 1.   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_rescale(pth_AI, 3, 3);
```

This would re-scale the given path to three times its original size.
