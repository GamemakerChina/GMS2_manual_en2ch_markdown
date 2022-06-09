# string_copy

With this function you can easily select a number of characters from
within a string to be copied to another one. The first character in a
string is always indexed as 1 and not 0 as you may expect, so to copy
(for example) the first five characters of string you would have
string_copy(str, 1, 5) . A further example is provided below.

#### Syntax:

``` gml
string_copy(str, index, count);
```

|          |                                                                        |                                                                                  |
|----------|------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Argument | Type                                                                   | Description                                                                      |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to copy from.                                                         |
| index    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The position of the first character in the string to copy from (numbered from 1) |
| count    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The number of characters, starting from the position of the first, to copy       |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
name = keyboard_string;
if (string_length(name) &amp;gt; 15)
{
    keyboard_string = string_copy(name, 1, 15);
}
```

The above code will allow the player to input a string through the
keyboard which is then stored in the variable name . This variable is
then checked to see if it exceeds the maximum length of 15 characters
and if it does, the keyboard_string is replaced by a 15 character copy
of the name string. This effectively limits the player input to 15
characters.
