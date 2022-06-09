# file_attributes

You can use this function to check the attributes of a given file. You
can add up the following constants to see the type of files you want:

|                |                 |
|----------------|-----------------|
| Constant       | Description     |
|  fa_readonly   | Read-only files |
|  fa_hidden     | Hidden files    |
|  fa_sysfile    | System files    |
|  fa_volumeid   | Volume-id files |
|  fa_directory  | Directories     |
|  fa_archive    | Archived files  |

**NOTE** : This is a Windows only function.

#### Syntax:

``` gml
file_attributes(fname, attr);
```

|          |                                                                                                                            |                                |
|----------|----------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                                       | Description                    |
| fname    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | The name of the file to check. |
| attr     |  [File Attribute Constant](../../../../../GameMaker_Language/GML_Reference/File_Handling/File_System/file_find_first)  | The attributes to check for.   |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !file_attributes(file, fa_hidden)
{
    file_delete(file);
}
```

This would check a file to see if it is hidden or not, and if not it is
deleted.
