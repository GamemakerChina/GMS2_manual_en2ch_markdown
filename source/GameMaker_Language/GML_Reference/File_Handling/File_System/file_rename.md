# file_rename

This function will rename the specified file with the specified name.
The function will return true if the file has successfully been renamed,
or false in any other circumstances. **WARNING!** This function may not
work as you expect due to GameMaker being sandboxed! Please see the
section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
file_rename(oldname, newname);
```

|          |                                                                           |                                 |
|----------|---------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                      | Description                     |
| oldname  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to change. |
| newname  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new name to give the file.  |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if file_exists("level1.txt")
{
    file_rename("level1.txt", "level.txt");
}
```

This would check for a file and if it exists it is renamed.
