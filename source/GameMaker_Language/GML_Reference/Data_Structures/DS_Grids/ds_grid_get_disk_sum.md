# ds_grid_get_disk_sum

This function can be used to add all the values all the cells found
within the defined disk area of a grid together, as shown in the image
below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_get_disk_sum.png)  

#### Syntax:

``` gml
ds_grid_get_disk_sum(index, xm, ym, r);
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
val = ds_grid_get_disk_sum(grid, 5, 5, 2)
```

The above code will set the variable "val" to the sum of all values
contained within the given disk of the DS grid indexed in the variable
"grid".
