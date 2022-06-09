# string_char_at

You can use this function to return a specific character at a specific
position within a string, with the index starting at 1 for the first
character. If no character is found or the string is shorter than the
given index value, an empty string "" is returned, however if the given
index is equal to or smaller than 0, then the first character of the
string is returned.

#### Syntax:

``` gml
string_char_at(str, index);
```

|          |                                                                        |                                         |
|----------|------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                   | Description                             |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to check.                    |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The position to get the character from. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = "Hello World";
str2 = string_char_at(str1, 7);
```

This will set str2 to the seventh character ("H" counting as the 1st) in
string str1 , in this case "W".
