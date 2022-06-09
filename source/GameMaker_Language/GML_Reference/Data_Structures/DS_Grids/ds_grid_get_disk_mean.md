# ds_grid_get_disk_mean

This function can be used to find the mean value for all the cells found
within the defined disk area of a grid (all cell values are added
together and then divided by the total number of cells that make up the
disk), as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_get_disk_mean.png)  

#### Syntax:

``` gml
ds_grid_get_disk_mean(index, xm, ym, r);
```

|          |                                                                                                             |                                         |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                        | Description                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                  |
| xm       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the disk on the grid. |
| ym       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the disk on the grid. |
| r        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The radius of the disk on the grid.     |

#### Returns:

``` gml
 Real

or

 String
```

#### Example:

``` gml
val = ds_grid_get_disk_mean(grid, 5, 5, 2)
```

The above code will set the variable "val" to the mean value contained
within the given disk of the DS grid indexed in the variable "grid".
