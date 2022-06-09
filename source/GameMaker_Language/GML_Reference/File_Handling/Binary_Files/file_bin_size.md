# file_bin_size

This function will return the size (in bytes) of a file that has been
opened for reading and/or writing. The File ID is the value returned by
the function [ file_bin_open() ](file_bin_open) . **NOTE** : These
functions **do not** work when the target module is HTML5.

#### Syntax:

``` gml
file_bin_size(binfile);
```

|          |                                                                                                                  |                                        |
|----------|------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                             | Description                            |
| binfile  |  [Binary File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Binary_Files/file_bin_open)  | The ID of the file to get the size of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
file = file_bin_open("myfile.bin", 2); size = file_bin_size(file); file_bin_close(file);
```

This would open a file from the local directory of the game, and assign
its index to the variable "file". It would then get the size of that
file and close it again.
