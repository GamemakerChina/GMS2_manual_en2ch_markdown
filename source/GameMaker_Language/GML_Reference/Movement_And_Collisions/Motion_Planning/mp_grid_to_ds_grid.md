# mp_grid_to_ds_grid

With this function you can copy the given MP grid into a
[DS grid](../../Data_Structures/DS_Grids/DS_Grids) . The DS grid
should be the same size as the MP grid, although it doesn't have to be
(data will be lost if it is smaller, and if it is larger all extra grid
cells will be 0). A cell in the DS grid will contain the value -1 if it
was flagged as occupied in the MP grid, or 0 if it wasn't.

#### Syntax:

``` gml
mp_grid_to_ds_grid(source, destination);
```

|             |                                                                                                                            |                                                                   |
|-------------|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument    | Type                                                                                                                       | Description                                                       |
| source      |  [MP Grid ID](../../../../../GameMaker_Language/GML_Reference/Movement_And_Collisions/Motion_Planning/mp_grid_create)  | Index of the mp_grid that is to be used                           |
| destination |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)                 | Index of the ds_grid that is to be used to copy the grid data to. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
motion_grid = ds_grid_create(room_width / 32, room_height / 32);
mp_grid_to_ds_grid(mp_grid, motion_grid);
```

The above code will create a new DS grid and then copy the MP grid data
contained in the variable "mp_grid" into the new DS grid.
