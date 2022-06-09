# file_text_open_append

This function opens the text file with the indicated filename for
*writing* (if the file does not exist, it is created), returning the
unique *id* of the file that which should be stored in a variable as it
will be used for all further actions to do with that file. The position
within the file for writing to is set to the last line of text that the
file contains. Note that if the file *can't* be created (because of an
illegal filename, for example) the function will return -1. **NOTE** :
You can only have a maximum of 32 files open at any one time. You should
also **always** close files when finished as this writes the information
and frees the memory associated with the file. **WARNING!** This
function may not work as you expect due to GameMaker being sandboxed!
Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
file_text_open_append(fname);
```

|          |                                                                           |                                    |
|----------|---------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                      | Description                        |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to append to. |

#### Returns:

``` gml
 Text File ID

or -1
```

#### Example:

``` gml
file = file_text_open_append(working_directory + "save.txt");
```

This would open "save.txt" from the same directory as the game and store
the file id in the variable "file".
