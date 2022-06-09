# string_format

Turns a real number into a string using your own formatting, where you
can choose how many "places" are saved to the string and how many
decimal places are saved also. Both can be very handy, some games prefer
to display a score as a set number of digits, while control over decimal
places can be good for a high accuracy the two decimal places of [
string() ](string) cannot provide. If the number of places specified
is greater than the value to be shown and/or the number plus the decimal
places that have been specified is less than the total places, then
spaces will be added before the value to make up the difference (see the
example below). Zeros will be added to the right of the decimal point if
the value given is less than the total and the number of decimal places
to include. The default format is no extra spaces on the left, and only
two decimal places on the right, eg "265.73".

#### Syntax:

``` gml
string_format(val, tot, dec);
```

|          |                                                                      |                                                                                                             |
|----------|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                 | Description                                                                                                 |
| val      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The real number to be turned into a string.                                                                 |
| tot      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The total number of places of the main number to be shown. Zeroes or spaces will be inserted to match this. |
| dec      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number of decimal places to be included.                                                                |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = string_format(1234, 8, 0);
str2 = string_format(pi, 1, 10);
str3 = string_format(pi, 5, 5);
```

This will set str1 to "    1234", str2 to "3.1415926535" and str3 to
"    3.14159".
