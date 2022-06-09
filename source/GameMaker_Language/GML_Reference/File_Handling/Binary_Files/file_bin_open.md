# file_bin_open

This function will open the binary file with the indicated name. The
mode indicates what can be done with the file:

-   0 = reading
-   1 = writing
-   2 = both reading and writing

When the file does not exist it is created, and the function returns the
id of the file that must be used in the other functions. You can open
multiple files at the same time (32 max), but don't forget to close them
once you are finished with them. **WARNING!** This function may not work
as you expect due to GameMaker being sandboxed! Please see the section
on the [File
System](../../../../Additional_Information/The_File_System) for more
information. **NOTE** : These functions **do not** work when the target
module is HTML5.

#### Syntax:

``` gml
file_bin_open(fname, mode);
```

|          |                                                                           |                                                  |
|----------|---------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                      | Description                                      |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to read from.               |
| mode     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The indicator of what can be done with the file. |

#### Returns:

``` gml
 Binary File ID
```

#### Example:

``` gml
file = file_bin_open("myfile.bin", 2);
```

This would open a file from the same directory as the game, and assign
its index to the variable "file".
