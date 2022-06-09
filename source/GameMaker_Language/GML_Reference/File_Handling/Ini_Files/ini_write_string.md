# ini_write_string

You can use this function to write a string (text) to an ini data file.
Ini Files are split into **sections** and then each section is
subsequently split into **key** - **value** pairs. So a typical ini file
would look something like this:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Files/IniExample.png)  
It is worth noting that using quotes and escape characters when writing
ini strings may cause issues when later reading back the data as it may
be prematurely truncated. For example, writing this will be an issue:

``` gml
ini_write_string("test2", "section", "hello \"Fritz\"");
```

#### Syntax:

``` gml
ini_write_string(section, key, value);
```

|          |                                                                           |                                                              |
|----------|---------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument | Type                                                                      | Description                                                  |
| section  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The section of the .ini to write to.                         |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The key within the relevant section of the .ini to write to. |
| value    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to write to the relevant destination.             |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
ini_open("savedata.ini");
ini_write_string("Save", "Player", global.Name);
ini_close();
```

The above code opens an ini file for reading and writing, then writes
the string stored in the global variable "Name" to the section "Save"
with the key "Player" before closing the file again.
