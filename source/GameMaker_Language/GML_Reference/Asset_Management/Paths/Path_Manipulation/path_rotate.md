# path_rotate

You can use this function to rotate a given path around its center.
Remember that in GameMaker (unless you are using physics) the angles are
calculated counter-clockwise, so rotating the path by 90 degrees would
rotate the path to the *left* . **This function changes the actual path
resource** , and so will permanently affect how the path is used by all
instances in the game from the moment the function is used until the end
of the game. If this is not what you require, then you should use a
function like [path_duplicate()](path_duplicate) to create a copy of
the path first, then call this function on the duplicated asset (don't
forget to call [path_delete()](path_delete) on the asset when it is
no longer required).  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Paths/pathrotated.png)  
**NOTE** : Once a path has been assigned to an instance using the
[path_start()](../path_start) function, you can use the
[path_orientation](../Path_Variables/path_orientation) variable to
change the path rotation too.

#### Syntax:

``` gml
path_rotate(index, angle);
```

|          |                                                                            |                                |
|----------|----------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                       | Description                    |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to flip. |
| angle    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The angle of rotation degrees. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_rotate(pth_Patrol, 90);
```

This would rotate the given 90 degrees counterclockwise.
