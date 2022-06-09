# ds_grid_read

This function can be used to convert a string which has been created
previously by the function [ ds_grid_write() ](ds_grid_write) back
into a DS grid. The DS grid must have been created previously (see the
example below). Note that if the specified DS string was written by the
GameMaker: Studio 1.2.x runtime (or older), you should specify the
optional argument "legacy", setting it to true as the string format
changed after that.

#### Syntax:

``` gml
ds_grid_read(index, string [, legacy]);
```

|          |                                                                                                             |                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument | Type                                                                                                        | Description                                                       |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid to read.                                    |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The string to read into the DS grid.                              |
| legacy   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                   |  OPTIONAL Can be either true or false or omitted completely.      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
grid = ds_grid_create(room_width div 32, room_height div 32);
ini_open("Save.ini");
ds_grid_read(grid, ini_read_string("Save", "0", ""));
ini_close();
```

The above code creates a DS grid based on the size of the room (each
32x32 square of pixels represents one grid cell) and then reads a
previously saved set of grid data from an ini file into the new DS grid.
