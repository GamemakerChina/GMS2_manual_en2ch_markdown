# string_byte_at

Returns the raw byte value as a real value at a given position in the
given string.

#### Syntax:

``` gml
string_byte_at(str, index);
```

|          |                                                                        |                                    |
|----------|------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                   | Description                        |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to check.               |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The position to get the byte from. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
newbyte = string_byte_at("Hello World", 5);
```

This will set newbyte to the raw byte value of the sixth letter of
"Hello World".
