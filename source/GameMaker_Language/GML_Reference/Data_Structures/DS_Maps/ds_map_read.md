# ds_map_read

This function will take a string that has previously been created by the
function [ ds_map_write() ](ds_map_write) and then read it into a
previously created DS map. If the map that the string is being read into
contains any key/value pairs, these will be cleared first before the
saved map is re-constructed. Note that if the specified DS string was
written by the GameMaker: Studio 1.2.x runtime (or older), you should
specify the optional argument "legacy", setting it to true as the string
format changed after that.

#### Syntax:

``` gml
ds_map_read(id, str, [legacy]);
```

|          |                                                                                                          |                                                                   |
|----------|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument | Type                                                                                                     | Description                                                       |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The id of the data structure to read the string into              |
| str      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                 | The string to read                                                |
| legacy   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                |  OPTIONAL Can be either true or false or omitted completely.      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
inventory = ds_map_create();
ini_open("map.ini");
var t_string = ini_read_string("Saved", "0", "");
if (t_string != "")
{
    ds_map_read(inventory, t_string);
}
ini_close();
```

The above code creates a new DS map and stores its id index in the
variable "inventory". It then opens an ini file and reads a string from
that file into the temporary variable "t_string". Finally, it checks to
make sure that the string is valid (not the default ini value of "") and
if it is it then reads the string into the newly created DS map before
closing the ini again.
