# ds_grid_get_mean

This function can be used to find the mean value for all the cells found
within the defined region of a grid (all cell values are added together
and then divided by the total number of cells that make the region), as
shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_get_mean.png)  

#### Syntax:

``` gml
ds_grid_get_mean(index, x1, y1, x2, y2);
```

|          |                                                                                                             |                                      |
|----------|-------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                        | Description                          |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.               |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The left cell column of the region.  |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The top cell row of the region.      |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The right cell column of the region. |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The bottom cell row of the region.   |

#### Returns:

``` gml
 Real

or

 String
```

#### Example:

``` gml
val = ds_grid_get_mean(grid, 0, 0, 5, 5)
```

The above code will set the variable "val" to the mean value contained
within the given region of the DS grid indexed in the variable "grid".
