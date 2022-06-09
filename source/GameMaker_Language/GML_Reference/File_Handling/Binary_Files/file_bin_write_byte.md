# file_bin_write_byte

This function will write a byte of data to the file identified by the
file ID at the current write position. You supply the file ID value, as
returned by the function [ file_bin_open() ](file_bin_open) and the
byte of data to write. **NOTE** : These functions **do not** work when
the target module is HTML5.

#### Syntax:

``` gml
file_bin_write_byte(binfile, byte);
```

|          |                                                                                                                  |                                 |
|----------|------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                             | Description                     |
| binfile  |  [Binary File ID](../../../../../GameMaker_Language/GML_Reference/File_Handling/Binary_Files/file_bin_open)  | The ID of the file to write to. |
| byte     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | The data to write.              |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
file_bin_write_byte(file, data);
```

This would write a byte to the selected file.
