# ds_grid_clear

This function can be used to clear a given DS grid to a specific value.
All cells within the grid will then contain this value, which can be a
real number or a string. The image below illustrates how this works:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_clear.png)  

#### Syntax:

``` gml
ds_grid_clear(index, val);
```

|          |                                                                                                             |                                   |
|----------|-------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                        | Description                       |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid to clear.  |
| val      |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The new value for all grid cells. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ds_grid_resize(global.Grid, room_width / 32, room_height / 32); ds_grid_clear(global.Grid, -1)
```

The above code will resize the DS grid indexed in the global variable
"Grid" and then clear it so that each cell holds the value -1.
