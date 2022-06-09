# file_bin_position

This function will returns the current position in bytes, where 0 is the
first position, of the file with the given file id. You supply the file
ID value, as returned by the function [ file_bin_open()
](file_bin_open) . **NOTE** : These functions **do not** work when
the target module is HTML5.

#### Syntax:

``` gml
file_bin_position(binfile);
```

|          |                                                                                                                  |                                            |
|----------|------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                             | Description                                |
| binfile  |  [Binary File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Binary_Files/file_bin_open)  | The ID of the file to get the position in. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
pos = file_bin_position(file);
```

This would store the current position in the variable "pos".
