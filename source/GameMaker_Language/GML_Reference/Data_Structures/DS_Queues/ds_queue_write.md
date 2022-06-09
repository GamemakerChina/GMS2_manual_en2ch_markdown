# ds_queue_write

This function returns a string which can then be stored or transferred
to another data structure using the [ ds_queue_read()
](ds_queue_read) function. **NOTE** : The returned string is not a
human readable string, but rather a dump of the contents of the
data-structure

#### Syntax:

``` gml
ds_queue_write(id);
```

|          |                                                                                                                |                                        |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                           | Description                            |
| id       |  [DS Queue ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Queues/ds_queue_create)  | The id of the data structure to write. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open("save.ini"); var str =ds_queue_write(queue); ini_write_string("Queues", "0", str); ds_queue_clear(queue);
 ini_close();
```

The above code opens an ini file and then writes a string containing the
information stored in the DS queue indexed in the variable "queue". The
queue is then cleared and the ini file closed.
