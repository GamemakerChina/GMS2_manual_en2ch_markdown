# buffer_base64_decode

With this function you can decode a base64 encoded string (created using
the [ buffer_base64_encode() ](buffer_base64_encode) function) into
a buffer. This function will create the buffer (as a 1 byte aligned
"grow" buffer") and return the unique index for the buffer which should
be used in all further function calls. **NOTE** : It's important that
you remove any dynamically created resources like this from memory when
you no longer need them to prevent memory leaks, so when you are
finished with the buffer that you have created you should free it up
again using [ buffer_delete() ](buffer_delete) .

#### Syntax:

``` gml
buffer_base64_decode(string);
```

|          |                                                                        |                                     |
|----------|------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                   | Description                         |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The base64 encoded string to decode |

#### Returns:

``` gml
 Buffer ID
```

#### Example:

``` gml
ini_open("Save.ini");
buff = buffer_base64_decode(ini_read_string("Save", "Slot1", ""));
ini_close();
```

The above code will open an ini file and then read a string from it into
the decode function. This function will return a buffer index, which is
stored in the variable "buff", containing the data previously encoded
and saved. The ini file is then closed.
