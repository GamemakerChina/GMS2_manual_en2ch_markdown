# file_delete

This function will delete the specified file from the system. It should
be noted that this function will only delete those files that GameMaker
is able to create and parse: ini files, text files and binary files, or
those files made to store game created resources like sprites or
surfaces. However, it will *not* delete any other file. The function
will also return true if the file has successfully been removed, or
false in any other circumstances. **WARNING!** This function may not
work as you expect due to GameMaker being sandboxed! Please see the
section on [File System
Limits](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
file_delete(fname);
```

|          |                                                                           |                                 |
|----------|---------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                      | Description                     |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to delete. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if file_exists("level.txt")
{
    file_delete("level.txt");
}
```

This would check for a file and if it exists it is deleted.
