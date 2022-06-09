# file_text_open_write

This function opens the text file with the indicated filename for
*writing only* (if the file does not exist, it is created), returning
the unique *id* of the file that which should be stored in a variable as
it will be used for all further actions to do with that file. Note that
if the file *can't* be created (because of an illegal filename, for
example) the function will return -1. **NOTE** : You can only have a
maximum of 32 files open at any one time. You should also **always**
close files when finished as this writes the information and frees the
memory associated with the file. **WARNING!** This function may not work
as you expect due to GameMaker being sandboxed! Please see the section
on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
file_text_open_write(fname);
```

|          |                                                                           |                                   |
|----------|---------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                      | Description                       |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to write to. |

#### Returns:

``` gml
 Text File ID

or -1
```

#### Example:

``` gml
var file;
file = file_text_open_write(working_directory + "level.txt");
file_text_write_string(file, level_data);
file_text_close(file);
```

The above code will open the file "level.txt" for writing and then write
the string stored in the variable "level_data" before finally closing
the file again.
