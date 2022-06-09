# mp_grid_get_cell

With this function you can check any given cell of the mp_grid to see if
it has been flagged as occupied or not, giving the index of the
(previously created) mp_grid and the x an y coordinates of the cell to
check. If it has been occupied or the position being checked is out of
the grid's bounds, the function will return -1; otherwise it will return
0.

#### Syntax:

``` gml
mp_grid_get_cell(id, x , y);
```

|          |                                                                                                                            |                                         |
|----------|----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                       | Description                             |
| id       |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be used |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The x coordinate of the grid to check.  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The y coordinate of the grid to check.  |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if mp_grid_get_cell(grid, mouse_x div 16, mouse_y div 16) == -1
{
    image_blend = c_red;
}
else
{
    image_blend = c_lime;
}
```

The above code will check the mp_grid cell that corresponds to the mouse
position and if it is occupied it sets the image_blend variable to red,
and if it is not occupied it sets it to green.
