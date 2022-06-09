# keyboard_string

This variable holds a string containing the last (at most) 1024
characters typed on the keyboard. This string will only contain
printable characters typed, but it *will* correctly respond to pressing
the backspace key by erasing the last character. This variable is *not*
read only and you can change it, for example to set it to "" (an empty
string) if you handled it already, and you can use the [String
Functions](../../Strings/Strings) to manipulate it. Note that when
using the on-screen [Virtual
Keyboard](../Virtual_Keys_And_Keyboards/Virtual_Keys_And_Keyboards)
, *only* this variable will be updated with the keyboard input.

#### **Syntax:**

``` gml
keyboard_string;
```

#### **Returns:**

``` gml
 String
```

#### **Example:**

``` gml
if string_length(keyboard_string) &amp;gt; 15
{
    keyboard_string = string_copy(keyboard_string, 1, 15);
}
```

The above code will limit the length of the keyboard string to 15
characters, removing those that are over that limit by copying the first
fifteen characters back into the variable.
