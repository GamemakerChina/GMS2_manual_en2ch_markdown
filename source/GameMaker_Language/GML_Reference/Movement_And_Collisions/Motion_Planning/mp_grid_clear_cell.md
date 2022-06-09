# mp_grid_clear_cell

This function can be used to clear a specific "cell" of an MP grid.
Cells are *not* calculated as room coordinates, but rather as grid
coordinates, where (0,0) is the top let corner of the grid. this means
that to clear a cell at a specific position in the room, we must change
the x and y coordinates into cell coordinate dividing them by the
resolution of the MP grid. The code example below shows how this works.

#### Syntax:

``` gml
mp_grid_clear_cell(id, h, v);
```

|          |                                                                                                                            |                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                                       | Description                              |
| id       |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be used  |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | Horizontal position of the cell to clear |
| v        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | vertical position of the cell to clear   |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
with (obj_Box)
{
    mp_grid_clear_cell(grid, floor(x / 32), floor(y /32));
    instance_destroy();
}
```

The above code will make all "obj_Box" destroy themselves and have them
mark the cells they occupied in the mp_grid indexed in the variable
"grid" as free. In this example, we find the appropriate cell by taking
the x/y coordinate of the object and dividing them by the resolution of
the grid (using floor to keep the values as integers).
