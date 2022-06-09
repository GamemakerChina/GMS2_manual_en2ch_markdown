# ds_grid_write

This function can be used to convert the given ds_grid into a string,
which can then be stored in an external file (for example). You can read
the returned string from this function back into a ds_grid using the
function [ ds_grid_read() ](ds_grid_read) . ** NOTE ** The returned
string is not a human readable string, but rather a dump of the contents
of the data-structure.

#### Syntax:

``` gml
ds_grid_write(index);
```

|          |                                                                                                             |                                 |
|----------|-------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                        | Description                     |
| index    |  [DS Grid ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Grids/ds_grid_create)  | The index of the grid to write. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open("Save.ini"); ini_write_string("Save", "0", ds_grid_write(mygrid)); ini_close()
```

The above code will open an ini file (creating it if it doesn't already
exist) and then write the given ds_grid as a string to that file.
