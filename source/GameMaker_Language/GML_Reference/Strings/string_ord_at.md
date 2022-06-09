# string_ord_at

You can use this function to return a specific character code at a
specific position within a string, with the index starting at 1 for the
first character. If no character is found or the string is shorter than
the value given to index, -1 is returned.

#### Syntax:

``` gml
string_ord_at(str, index);
```

|          |                                                                        |                                              |
|----------|------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                   | Description                                  |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to check.                         |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The position to get the character code from. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
str = "Hello World"; char_code = string_ord_at(str, 7);
```

This will get the character code for the seventh character (where "H"
counts as the first) in string "str" and store it in the variable
"char_code".
