# ansi_char

This function returns a string containing the character with raw BYTE
value set. This will not, *and should not* , be displayed, but it will
save correctly to disk for use in encoding.

#### Syntax:

``` gml
ansi_char(val);
```

|          |                                                                      |                     |
|----------|----------------------------------------------------------------------|---------------------|
| Argument | Type                                                                 | Description         |
| val      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The raw byte value. |

#### Returns:

``` gml
 String

(Single character)
```

#### Example:

``` gml
var str1 = ansi_char($EF); var str2 = ansi_char($BB); var str3 = ansi_char($BF); file_text_write_string(global.saveFile, str1 + str2 + str3);
```

The above code creates a string from raw byte data and writes it to a
(previously opened) file.
