# real

This function can be used to turn a given string into a real number.
When using this function, numbers, minus signs, decimal points and
exponential parts in the string are taken into account, while other
characters (such as letters) will cause an error to be thrown. If you
know, or suspect, that a string may have other characters then you can
use [ string_digits() ](string_digits) to remove all non-numeric
characters, before using this function to turn the resulting string into
a real number.

#### Syntax:

``` gml
real(string);
```

|          |                                                                        |                                             |
|----------|------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                   | Description                                 |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to be converted to a real value. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var t_str = string_digits(input_str); age = real(t_str);
```

The above code will take the input string, strip it of all characters
other than numbers and then set the variable "age" to hold the real
number value of the return string.
