# ds_grid_set_region

This function can be used to set a rectangular region of a given grid to
a specified value (which can be either a real or a string) as
illustrated by the image shown below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_set_region.png)  

#### Syntax:

``` gml
ds_grid_set_region(index, x1, y1, x2, y2, val);
```

|          |                                                                                                             |                                                         |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                             |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid.                                  |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the left of the region in the grid.   |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the top of the region in the grid.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the right of the region in the grid.  |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the bottom of the region in the grid. |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value to set the region cells to.                   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_set_region(grid, 5, 5, 10, 10, 99)
```

This would set all cells within the region of the grid indexed in the
variable "grid" from (5,5) to (10,10) to 99.
