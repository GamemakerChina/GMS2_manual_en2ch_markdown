# path_flip

This function takes all the path points and flips them along the
horizontal axis. **This function changes the actual path asset** , and
so will permanently affect how the path is used by all instances in the
game from the moment the function is used until the end of the game.If
this is not what you require, then you should use a function like
[path_duplicate()](path_duplicate) to create a copy of the path
first, then call this function on the duplicated asset (don't forget to
call [path_delete()](path_delete) on the asset when it is no longer
required).  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Paths/pathflip.png)  

#### Syntax:

``` gml
path_flip(index);
```

|          |                                                               |                                |
|----------|---------------------------------------------------------------|--------------------------------|
| Argument | Type                                                          | Description                    |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)  | The index of the path to flip. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_flip(mypath);
```

This would flip the path indexed in the variable "mypath" along the
horizontal axis.
