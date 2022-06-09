# ds_priority_write

This function returns a string which can then be stored or transferred
to another data structure using the [ ds_priority_read()
](ds_priority_read) function. **NOTE** : The returned string is not
a human readable string, but rather a dump of the contents of the
data-structure

#### Syntax:

``` gml
ds_priority_write(id);
```

|          |                                                                                                                               |                                        |
|----------|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                          | Description                            |
| id       |  [DS Priority ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Priority_Queues/ds_priority_create)  | The id of the data structure to check. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var str;
ini_open("save.ini");
str = ds_priority_write(p_queue);
ini_write_string("P_Queues", "0", str);
ds_priority_clear(p_queue);
ini_close();
```

The above code opens an ini file and then writes a string containing the
information stored in the DS priority queue indexed in the variable
"p_queue". The priority queue is then cleared and the ini file closed.
