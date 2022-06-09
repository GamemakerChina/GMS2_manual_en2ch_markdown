# ds_grid_set_disk

With this function you can set a circular region of a grid to a certain
value. You need to supply a starting grid cell (as an x and y axis
coordinate) as well as the radius of the disk to set and the value that
you wish to set the disk too, as shown by the illustration below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_set_disk.png)  

#### Syntax:

``` gml
ds_grid_set_disk(index, xm, ym, r, val);
```

|          |                                                                                                             |                                                  |
|----------|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                        | Description                                      |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                           |
| xm       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the disk on the grid.          |
| ym       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the disk on the grid.          |
| r        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The radius of the disk on the grid.              |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to set with the cells within the disk. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_set_disk(grid, ds_grid_width(grid) div 2, ds_grid_height(grid) div 2, 5, -4)
```

The above code will set a circular region with a radius of 5 cells in
the DS grid indexed in the variable "grid" to a value of -4.
