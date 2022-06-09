# ini_key_exists

This function checks to see if a key exists in the currently open ini
and will return true if it does or false otherwise. This is not a
necessary check to prevent errors as, when a key does not exist, reading
from a non-existent key will just return a default value. It can be
useful to see if an ini file has saved specific data and a few other
things, however.

#### Syntax:

``` gml
ini_key_exists(section, key);
```

|          |                                                                           |                                                      |
|----------|---------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                      | Description                                          |
| section  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The section in the open .ini file to check a key in. |
| key      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The key to check for.                                |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
ini_open("savedata.ini");
if !ini_key_exists("save1", "name")
{
    global.name = "Player1";
}
ini_close();
```

This will set variable global.name to "Player1" if no such key as "name"
exists.
