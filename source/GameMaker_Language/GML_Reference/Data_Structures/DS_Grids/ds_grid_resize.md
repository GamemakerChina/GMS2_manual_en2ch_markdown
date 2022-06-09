# ds_grid_resize

With this function you can resize the given DS grid to have a different
width and/or height. If the grid size is larger than the current grid,
the new cells will have a base value of 0, and if the size is smaller
then the values held in the cells that are no longer within the new size
will be lost. All other cells will be left untouched.

#### Syntax:

``` gml
ds_grid_resize(index, w, h);
```

|          |                                                                                                             |                                   |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                        | Description                       |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid to resize. |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The new width of the grid.        |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The new height of the grid.       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_resize(global.Grid, room_width / 32, room_height / 32); ds_grid_clear(global.Grid, -1)
```

The above code will resize the DS grid indexed in the global variable
"Grid" and then clear it so that each cell holds the value -1.
