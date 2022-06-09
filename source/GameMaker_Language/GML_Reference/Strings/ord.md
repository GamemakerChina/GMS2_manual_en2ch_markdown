# ord

This function takes a single character input string and returns the
Unicode (UTF8) value for that character. Note that when used with the [
keyboard_check\* ](../Game_Input/Keyboard_Input/Keyboard_Input)
functions, the input string can only be one character in length and can
only be a number from 0 to 9 or a *capitalised* Roman character from A
to Z.

#### Syntax:

``` gml
ord(string);
```

|          |                                                                        |                                                  |
|----------|------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                   | Description                                      |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string with which to find the Unicode value. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if keyboard_check(ord("W"))
{
    y -= 4;
}
```

This will move the calling instance four pixels upwards if the key W is
held down.
