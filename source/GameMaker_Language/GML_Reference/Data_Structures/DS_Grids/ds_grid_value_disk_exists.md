# ds_grid_value_disk_exists

With this function you can check to see if a specific value (real or
string) is present within a circular area of a given DS grid. If it is
present the function will return true otherwise it will return false .

#### Syntax:

``` gml
ds_grid_value_disk_exists(index, xm, ym, r, val);
```

|          |                                                                                                             |                                         |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                        | Description                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                  |
| xm       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the disk on the grid. |
| ym       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the disk on the grid. |
| r        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The radius of the disk on the grid.     |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to find.                      |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if ds_grid_value_disk_exists(grid, 5, 5, 5, val)
{
    xpos = ds_grid_value_disk_x(grid, 5, 5, 5, val);
    ypos = ds_grid_value_disk_y(grid, 5, 5, 5, val);
}
```

The above code checks a DS grid for a specific value within a disk
region. if it is found, it then stores the x and y position of the value
in two variables for later use.
