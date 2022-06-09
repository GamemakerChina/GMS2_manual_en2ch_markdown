# file_text_open_from_string

This function will create a text file from a string and open it for
reading, returning the file "handle" that should be used in all further
file function calls to read from this file. Note that this file is
temporary and *read only* , and as such it will be removed from memory
the moment it is closed. **NOTE** : You can only have a maximum of 32
files open at any one time. You should also **always** close files when
finished as this writes the information and frees the memory associated
with the file. **WARNING!** This function may not work as you expect due
to GameMaker being sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
file_text_open_from_string(string);
```

|          |                                                                           |                                     |
|----------|---------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                      | Description                         |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to create the file from. |

#### Returns:

``` gml
 Text File ID

or -1
```

#### Example:

``` gml
file = file_text_open_from_string(reset_str);
```

The above code takes the string stored in the variable "reset_str" and
uses it to create a read-only text file. The "handle" for this file is
then stored in the variable "file" for all further file functions to
use.
