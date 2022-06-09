# file_find_first

This function will return the name of the first file that satisfies the
mask and the attributes. If no such file exists, then an empty string is
returned. The mask can contain a path with wildcards, for example
C:\temp\\\*.doc . The attributes give the additional files you want to
see, so the normal files are always returned when they satisfy the mask.
You can add up the following constants to see the type of files you want
(using \| ). If you do not wish to add any attributes, use 0.

|                                                                                                                            |                 |
|----------------------------------------------------------------------------------------------------------------------------|-----------------|
|  [File Attribute Constant](../../../../../GameMaker_Language/GML_Reference/File_Handling/File_System/file_find_first)  |                 |
| Constant                                                                                                                   | Description     |
|  fa_readonly                                                                                                               | Read-only files |
|  fa_hidden                                                                                                                 | Hidden files    |
|  fa_sysfile                                                                                                                | System files    |
|  fa_volumeid                                                                                                               | Volume-id files |
|  fa_directory                                                                                                              | Directories     |
|  fa_archive                                                                                                                | Archived files  |

Attributes can only be used on Windows. For all other platforms, use 0.
WARNING This function may not work as you expect due to GameMaker being
sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information. NOTE This function will not work at all on the HTML5
target.

#### Syntax:

``` gml
file_find_first(mask, attr);
```

|          |                                                                                                                                |                                          |
|----------|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                                           | Description                              |
| mask     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The mask to use for searching.           |
| attr     |  [File Attribute Constant](../../../../../GameMaker_Language/GML_Reference/File_Handling/File_System/file_find_first) (s)  | The specific file attribute to look for. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if directory_exists("\User Content")
{
    fileA = file_find_first("/User Content/*.doc", fa_readonly);
    fileB = file_find_next();
    fileC = file_find_next();
    file_find_close();
}
```

This code checks if the specified directory exists and if it does, goes
there and returns the first "read only" .doc file found. It then looks
for two more files and closes the file finder. You can look for any
number of files using a
[while](../../../GML_Overview/Language_Features/while) loop:

``` gml
var files = [];
var file_name = file_find_first("/User Content/*.doc", fa_readonly);

while (file_name != "")
{
    array_push(files, file_name);

    file_name = file_find_next();
}

file_find_close();
```

The above code creates an empty array to store all the file names that
were found, and starts looking for read only .doc files. If that file
name is not an empty string, it pushes it into the files array, and then
attempts to find the next file. The loop will keep repeating until an
empty string is found (meaning there are no more matching files), which
is when it ends the loop and closes the file finder at the end.
