# environment_get_variable

This function returns the value (a string) of the environment variable
with the given name (also a string). You can get the available
environment variables on macOS and Ubuntu (Linux) by typing " env " into
the terminal app, and for information on Windows environment variables,
if you are using the command prompt then type " echo %PATH% ", and using
PowerShell it's " ls env ". Note that on both macOS and Ubuntu (Linux)
the "HOME" environment variable will return the " \~/ " path which maps
to " /Users/ " on macOS and " /home/ " on Ubuntu (Linux). **NOTE** :
This function is for Windows, macOS and Ubuntu (Linux) only.

#### Syntax:

``` gml
environment_get_variable(name);
```

|          |                                                                        |                                                           |
|----------|------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                   | Description                                               |
| name     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name (a string) of the environment variable to check. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
e_str = environment_get_variable("APPDATA");
```

The above code will return the full path for the environment variable "
%appdata% ", which is normally " C:\Users\\{username}\AppData\Roaming ".
