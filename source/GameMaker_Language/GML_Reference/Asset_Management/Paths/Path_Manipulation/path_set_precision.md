# path_set_precision

With this function you can change the "smoothness" of a path. This value
must be between 1 and 8, with a low value creating straighter edges with
sharper curves between points, while a higher value will round the
points and make the path a lot more "curvy". Note that this function
will have no visible effect if the path has not been set to smooth in
the path editor or using the function [ path_set_kind()
](path_set_kind) . **This function changes the actual path asset** ,
and so will permanently affect how the path is used by all instances in
the game from the moment the function is used until the end of the
game. If this is not what you require, then you should use a function
like [path_duplicate()](path_duplicate) to create a copy of the path
first, then call this function on the duplicated asset (don't forget to
call [path_delete()](path_delete) on the asset when it is no longer
required).  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Paths/setprecision.png)  

#### Syntax:

``` gml
path_set_precision(index, prec);
```

|          |                                                                            |                                                                |
|----------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                    |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to change.                               |
| prec     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The precision of the path. Must be an integer between 1 and 8. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_set_precision(pth_Patrol, 2);
```

This will set the precision of the given path to 2.
