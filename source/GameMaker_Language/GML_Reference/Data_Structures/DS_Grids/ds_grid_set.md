# ds_grid_set

This function can be used to set a given cell within the given DS grid
to any value, which can be a real number or a string. The image below
illustrates this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_set.png)  

#### Syntax:

``` gml
ds_grid_set(index, x, y, value);
```

|          |                                                                                                             |                                       |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                                                        | Description                           |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid.               |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The x position of the cell to set.    |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                      | The y position of the cell to set.    |
| value    |  [Variable](../../../../../GameMaker_Language/GML_Overview/Data_Types#variable)                         | The value with which to set the cell. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
grid = ds_grid_create(5, 5);
var i = 0;
var j = 0;

repeat (ds_grid_width(grid))
{
    repeat (ds_grid_height(grid))
    {
        ds_grid_set(grid, i, j, irandom(9));
        j += 1;
    }

    j = 0;
    i += 1;
}
```

The above code creates a grid and stores its index in the variable
"grid". It then populates this grid with random integers from 0 to 9.
