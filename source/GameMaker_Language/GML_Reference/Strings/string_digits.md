# string_digits

You can use this function to parse a given string and get any numbers
from it. For example, say you have this text - "I am 81 years old". With
this function you would get a return string of "81".

#### Syntax:

``` gml
string_digits(string);
```

|          |                                                                        |                                    |
|----------|------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                   | Description                        |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to get the digits from. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var t_str = string_digits(input_str); age = real(t_str);
```

The above code will take the input string, strip it of all characters
other than numbers and then set the variable age to hold the real number
value of the return string (so, if the input string was - for example -
"I am 18", the function would return "18").
