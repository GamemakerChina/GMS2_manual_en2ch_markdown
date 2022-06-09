# ds_grid_value_exists

With this function you can check to see if a specific value (real or
string) is present within a rectangular area of a given DS grid. If it
is present the function will return true otherwise it will return false
.

#### Syntax:

``` gml
ds_grid_value_exists(index, x1, y1, x2, y2, val);
```

|          |                                                                                                             |                                                         |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                                  |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the left of the region in the grid.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the top of the region in the grid.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the right of the region in the grid.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the bottom of the region in the grid. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to find.                                      |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if ds_grid_value_exists(grid, 0, 1, 5, 6, val)
{
    xpos = ds_grid_value_x(grid, 0, 1, 5, 6, val);
    ypos = ds_grid_value_y(grid, 0, 1, 5, 6, val);
}
```

The above code checks a DS grid for a specific value within a
rectangular region. if it is found, it then stores the x and y position
of the value in two variables for later use.
