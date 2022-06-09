# file_text_open_read

This function opens the text file with the indicated filename for
*reading only* , returning the unique id of the file that which should
be stored in a variable as it will be used for all further actions to do
with that file. If the file does not exists then the function will
return the value -1. **NOTE** : You can only have a maximum of 32 files
open at any one time. You should also **always** close files when
finished as this writes the information and frees the memory associated
with the file. **WARNING!** This function may not work as you expect due
to GameMaker being sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
file_text_open_read(fname);
```

|          |                                                                           |                                    |
|----------|---------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                      | Description                        |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to read from. |

#### Returns:

``` gml
 Text File ID

or -1
```

#### Example:

``` gml
file = file_text_open_read(working_directory + "level.txt");
```

This would open "level.txt" from the same directory as the game and
store the file id in the variable "file".
