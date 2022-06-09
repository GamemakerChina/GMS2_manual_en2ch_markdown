# string_byte_length

This function returns the number of bytes in a string, but you should
note that due to their being held as UTF8, this will *not* be equal to
their string length.

#### Syntax:

``` gml
string_byte_length(string);
```

|          |                                                                        |                                               |
|----------|------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                   | Description                                   |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to measure the number of bytes of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
bytesize = string_byte_length("Hello World");
```

This would set bytesize to the number of bytes in "Hello World".
