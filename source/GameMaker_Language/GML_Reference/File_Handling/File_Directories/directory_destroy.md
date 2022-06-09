# directory_destroy

This function will remove a directory with the given name in the save
area. **NOTE** : This function will not work on HTML5 as you cannot
create or remove directories in the browser local storage. **WARNING!**
This function may not work as you expect due to GameMaker being
sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information.

#### Syntax:

``` gml
directory_destroy(dname)
```

|          |                                                                           |                                      |
|----------|---------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                      | Description                          |
| dname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the directory to remove. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if directory_exists("DLC")
{
    directory_destroy("DLC");
}
```

This will check to see if the specified directory exists in the local
data folder and, if it does, it is removed.
