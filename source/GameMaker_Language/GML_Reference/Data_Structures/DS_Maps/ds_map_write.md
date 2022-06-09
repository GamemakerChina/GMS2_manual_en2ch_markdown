# ds_map_write

This function will turn the DS map data of the specified map into string
format which can then be written to an \*.ini or a \*.txt file for easy
storage. This string can then be later read back into a new ds_map using
[ ds_map_read() ](ds_map_read) . **NOTE** : The returned string is
not a human readable string, but rather a dump of the contents of the
data-structure.

#### Syntax:

``` gml
ds_map_write(id);
```

|          |                                                                                                          |                                     |
|----------|----------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                     | Description                         |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the data structure to use |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open("map.ini"); var t_string; t_string = ds_map_write(inventory); ini_write_string("Saved", "0", t_string); ini_close();
```

The above code opens an ini file ready to be written to. It then uses
ds_map_write() to generate a string which is stored in the temporary
variable "t_string". Finally, it writes that string to the ini file
before closing it.
