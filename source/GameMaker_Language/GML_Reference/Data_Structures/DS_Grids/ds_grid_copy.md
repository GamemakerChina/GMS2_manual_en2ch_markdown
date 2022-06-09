# ds_grid_copy

With this function you can copy the contents of one grid into another
one. Both grids must have been created previously using the [
ds_grid_create() ](ds_grid_create) function.

#### Syntax:

``` gml
ds_grid_copy(destination, source);
```

|             |                                                                                                             |                                      |
|-------------|-------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument    | Type                                                                                                        | Description                          |
| destination |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid to copy to.   |
| source      |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid to copy from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
n_grid = ds_grid_create(ds_grid_width(a_grid), ds_grid_height(a_grid));
ds_grid_copy(n_grid, a_grid);
ds_grid_clear(a_grid, -1)
```

The above code creates a new DS grid, based on the width and height of a
previously created grid, then copies the information form the previous
grid to the new one. Finally it clears the old grid so that all cells
have a value of -1.
