# ds_grid_sort

This function can be used to sort a DS grid based on the values from a
given column (much as you would sort files by date, size etc... in the
OS file explorer). The following image shows an example:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_sort.png)  

#### Syntax:

``` gml
ds_grid_sort(index, column, ascending);
```

|           |                                                                                                             |                                                                                 |
|-----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Argument  | Type                                                                                                        | Description                                                                     |
| index     |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid to sort.                                                  |
| column    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The column to use for sorting the rows                                          |
| ascending |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                   | Whether to sort lowest to highest ( true ), or highest to lowest ( false ).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_sort(grid, 3, false)
```

This would take all the values in the DS grid indexed in the variable
"grid" and sort them according to the values found in the 3rd column of
the grid (as shown in the above image).
