# ds_grid_get

This function can be used to get the value from any cell within the
given DS grid. If you pass invalid grid coordinates to the function,
then the value returned will be undefined and an error will be shown in
the output window.

#### Syntax:

``` gml
ds_grid_get(index, x, y);
```

|          |                                                                                                             |                                                           |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                               |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                                    |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the cell you want to find the value of. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the cell you want to find the value of. |

#### Returns:

``` gml
 Variable
```

#### Example:

``` gml
var xx = irandom(ds_grid_width(grid) - 1);
var yy = irandom(ds_grid_height(grid) - 1);
val = ds_grid_get(grid, xx, yy)
```

The above code selects a random cell from the DS grid indexed in the
variable "grid" and stores its value in the variable "val".
