# file_find_next

This function returns the name of the next file that satisfies the
previously given mask and the attributes (defined by [ file_find_first()
](file_find_first) ). If no such file exists, the empty string is
returned. WARNING This function may not work as you expect due to
GameMaker being sandboxed! Please see the section on the [File
System](../../../../Additional_Information/The_File_System) for more
information. NOTE This function works on all the C++ target platforms
(Windows, Mac, iOS, Android), BUT the filter flags only work on Windows.

#### Syntax:

``` gml
file_find_next();
```

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
