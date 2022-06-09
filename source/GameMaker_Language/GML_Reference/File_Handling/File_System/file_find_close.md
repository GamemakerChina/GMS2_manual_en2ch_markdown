# file_find_close

This function must be called after handling files opened using [
file_find_first() ](file_find_first) and [ file_find_next()
](file_find_next) functions to free memory. The file find functions
open handles into the file directory and these take up a minimal amount
of memory, which (over time) adds up. Therefore you should always call
this function after you have found the files you require to "close"
these handles.

#### Syntax:

``` gml
file_find_close();
```

#### Returns

``` gml
N/A
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
