# string_set_byte_at

This function sets a byte directly in a string (based on the UTF8
format) and returns a copy of the string with the changes. NOTE This
function is incredibly slow so consider carefully whether it is
necessary and where you use it.

#### Syntax:

``` gml
string_set_byte_at(str, pos, byte);
```

|          |                                                                        |                                                                       |
|----------|------------------------------------------------------------------------|-----------------------------------------------------------------------|
| Argument | Type                                                                   | Description                                                           |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to change the byte of.                                     |
| pos      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The position within the string (starting at 1) to change the byte of. |
| byte     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The new byte value.                                                   |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str = string_set_byte_at("hello", 2, 97);
```

The above code would change the byte value of the second letter in the
string, and so set the variable str to hold "hallo".
