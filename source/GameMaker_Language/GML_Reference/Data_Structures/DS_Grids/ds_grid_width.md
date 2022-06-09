# ds_grid_width

This function will return the width of the given grid. This value is the
number of cells the grid has along the x-axis and is always an integer,
as shown in the image below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Data_Structures/ds_grid_width.png)  

#### Syntax:

``` gml
ds_grid_width(index);
```

|          |                                                                                                             |                                              |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                        | Description                                  |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | This index of the grid to find the width of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; ds_grid_width(grid); ++i)
{
    for (var j = 0; j &amp;lt; ds_grid_height(grid); ++j)
    {
        if (ds_grid_get(grid, i, j) == 1)
        {
            instance_create_layer(i * 32, j * 32, "Walls", obj_Wall);
        }
    }
}
```

The above code will loop through the DS grid indexed in the variable
"grid" and if the value found in any specific cell is equal to 1, it
will then create an instance of "obj_Wall" at the appropriate position
within the room.
