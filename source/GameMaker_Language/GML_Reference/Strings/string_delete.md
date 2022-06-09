# string_delete

This function is used to remove a part of the given string. You supply
the input string, the starting position within that string to remove
characters from (the index starts at 1) and the number of characters to
remove. The function will return a new string without that part in it.

#### Syntax:

``` gml
string_delete(str, index, count);
```

|          |                                                                        |                                                         |
|----------|------------------------------------------------------------------------|---------------------------------------------------------|
| Argument | Type                                                                   | Description                                             |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to copy and delete from.                     |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The position of the first character to remove (from 1). |
| count    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The number of characters to remove.                     |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = "Helloo World";
str2 = string_delete(str1, 5, 1);
```

This will set str2 to "Hello World", as it removes the extra "o" from
"Hello" (which is present at position 5).
