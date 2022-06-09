# ds_stack_write

This function returns a string which can then be stored or transferred
to another data structure using the [ ds_stack_read()
](ds_stack_read) function. **NOTE** : The returned string is not a
human readable string, but rather a dump of the contents of the
data-structure

#### Syntax:

``` gml
ds_stack_write(id);
```

|          |                                                                                                                |                                        |
|----------|----------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                           | Description                            |
| id       |  [DS Stack ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Stacks/ds_stack_create)  | The id of the data structure to write. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
ini_open("save.ini"); var str = ds_stack_write(stack); ini_write_string("Stacks", "0", str); ds_stack_clear(stack);
 ini_close();
```

The above code opens an ini file and then writes a string containing the
information stored in the DS stack indexed in the variable "stack". The
stack is then cleared and the ini file closed.
