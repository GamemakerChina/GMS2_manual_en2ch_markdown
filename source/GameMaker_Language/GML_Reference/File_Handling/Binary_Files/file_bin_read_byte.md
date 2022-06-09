# file_bin_read_byte

This function will return a byte of data from current position within
the file with the given file ID. You supply the file ID value, as
returned by the function [ file_bin_open() ](file_bin_open) .
**NOTE** : These functions **do not** work when the target module is
HTML5.

#### Syntax:

``` gml
file_bin_read_byte(binfile);
```

|          |                                                                                                                  |                                          |
|----------|------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                             | Description                              |
| binfile  |  [Binary File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Binary_Files/file_bin_open)  | The ID of the file to get the data from. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
file = file_bin_open("myfile.bin", 2); data = file_bin_read_byte(file); file_bin_close(file);
```

This would open a file from the same directory as the game, and get a
byte of data from it before closing it again.
