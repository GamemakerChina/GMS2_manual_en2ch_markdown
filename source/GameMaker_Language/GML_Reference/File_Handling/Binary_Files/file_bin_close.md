# file_bin_close

Closes a previously opened binary file. You supply the file ID value, as
returned by the function [ file_bin_open() ](file_bin_open) .
**NOTE** : These functions **do not** work when the target module is
HTML5.

#### Syntax:

``` gml
file_bin_close(binfile);
```

|          |                                                                                                                  |                              |
|----------|------------------------------------------------------------------------------------------------------------------|------------------------------|
| Argument | Type                                                                                                             | Description                  |
| binfile  |  [Binary File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Binary_Files/file_bin_open)  | The ID of the file to close. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
file = file_bin_open("myfile.bin", 2); file_bin_rewrite(file);
 file_bin_close(file);
```

This would open a file from the same directory as the game, and assign
its index to the variable "file". It would then re-write the file
(clearing it of data), and close it again.
