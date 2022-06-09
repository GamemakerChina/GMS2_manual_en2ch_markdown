# ini_open_from_string

This function will create a temporary ini file from a string and open it
for reading/writing. The string should be correctly formatted as an ini
file (ie: with sections, line breaks keys and values) otherwise the ini
file will not be created correctly. Note that this ini file is temporary
and will be removed from memory the moment it is closed, losing any
information that was stored in it, however the [ ini_close()
](ini_close) function returns a string of the full ini file which
can then be saved to a server or to disk.

#### Syntax:

``` gml
ini_open_from_string(string);
```

|          |                                                                           |                                                |
|----------|---------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                      | Description                                    |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string containing all the ini information. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ini_open_from_string(str)
global.sound = ini_read_string("Options", "Sound", true);
ini_close();
```

The above code sets a temporary ini to hold the information from the
string "str", then reads from the ini before closing it again.
