# directory_exists

This function will return true if the indicated directory exists or
false if it does not. The specified name must include the full path, not
a relative path and by default you cannot access any directories from
out-with the game bundle as all games are sandboxed (see the section on
the [File
System](../../../../Additional_Information/The_File_System) for more
information).

#### Syntax:

``` gml
directory_exists(dname)
```

|          |                                                                           |                                        |
|----------|---------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                      | Description                            |
| dname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the directory to look for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if directory_exists(working_directory + "Saves/")
{
    file = file_find_first(working_directory + "Saves/*.doc", fa_readonly);
}
```

This will check to see if the specified directory exists then, if it
does, go there and return the first "read only" doc file found.
