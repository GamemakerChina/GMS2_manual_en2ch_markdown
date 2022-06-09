# path_set_kind

This function can be used to set the kind of path that you wish the
specified resource to be. This can be either a straight line path (set
to 0) or a smoothed path (set to 1) in which case the path precision has
to be taken into account too (the precision can be set too using [
path_set_precision() ](path_set_precision) ). This function changes
the actual path resource, and so will permanently affect how the path is
used by all instances in the game from the moment the function is used
until the end of the game.If this is not what you require, then you
should use a function like [path_duplicate()](path_duplicate) to
create a copy of the path first, then call this function on the
duplicated asset (don't forget to call [path_delete()](path_delete)
on the asset when it is no longer required).  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Paths/setkind.png)  

#### Syntax:

``` gml
path_set_kind(index, val);
```

|          |                                                                            |                                                       |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                       | Description                                           |
| index    |  [Path Asset](../../../../../../The_Asset_Editors/Paths)               | The index of the path to change.                      |
| val      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The kind of the path, 0 for straight or 1 for smooth. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
path_set_kind(pth_Patrol, true);
```

This will set the given path to be a "smooth" path.
