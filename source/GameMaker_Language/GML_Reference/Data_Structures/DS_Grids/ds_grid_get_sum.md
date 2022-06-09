# ds_grid_get_sum

This function can be used to add all the values all the cells found
within the defined region of a grid together, as shown in the image
below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_get_sum.png)  

#### Syntax:

``` gml
ds_grid_get_sum(index, x1, y1, x2, y2);
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
val = ds_grid_get_sum(grid, 0, 0, 5, 5)
```

The above code will set the variable "val" to the sum of all values
contained within the given region of the DS grid indexed in the variable
"grid".
