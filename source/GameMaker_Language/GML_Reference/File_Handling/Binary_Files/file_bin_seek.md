# file_bin_seek

This function moves the current read position within the file to the
indicated position. You supply the file ID value, as returned by the
function [ file_bin_open() ](file_bin_open) , and to append a file,
move the position to the size of the file before writing. **NOTE** :
These functions **do not** work when the target module is HTML5.

#### Syntax:

``` gml
file_bin_seek(binfile, pos);
```

|          |                                                                                                                  |                                      |
|----------|------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                             | Description                          |
| binfile  |  [Binary File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Binary_Files/file_bin_open)  | The ID of the file to read from.     |
| pos      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | The position in the file to move to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
file = file_bin_open("myfile.bin", 2); size = file_bin_size(file); file_bin_seek(file, size);
```

This would open a file from the same directory as the game, and assign
its index to the variable "file", then get the size of the file and set
the next writing position to that size.
