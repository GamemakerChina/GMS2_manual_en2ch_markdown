# ds_list_write

This function returns a string which can then be stored or transferred
to another data structure using the [ ds_list_read() ](ds_list_read)
function. **NOTE** : The returned string is not a human readable string,
but rather a dump of the contents of the data-structure.

#### Syntax:

``` gml
ds_list_write(id);
```

|          |                                                                                                             |                                        |
|----------|-------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                        | Description                            |
| id       |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)  | The id of the data structure to write. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open("save.ini"); var str = ds_list_write(list); ini_write_string("Lists", "0", str); ds_list_clear(list);
 ini_close();
```

The above code opens an ini file and then writes a string containing the
information stored in the DS list indexed in the variable "list". The
list is then cleared and the ini file closed.
