# string

With this function you can turn any real number into a string. If the
real number is an integer, it will be saved with no decimal places,
otherwise, it will be saved with two decimal places. If you require more
decimal places, then use the function [ string_format()
](string_format) . Also note that using this function on a variable
storing an [array](../../GML_Overview/Arrays) , a [data
structure](../Data_Structures/Data_Structures) , or a
[struct](../../GML_Overview/Structs) will convert the contents of
these variables into a string which can then be output to the console or
saved to a file for debugging.

#### Syntax:

``` gml
string(val);
```

|          |                                                                      |                                             |
|----------|----------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                 | Description                                 |
| val      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The real number to be turned into a string. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
draw_text(100, 100, "Score: " + string(score) + " / Health: " + string(health));
```

The above code uses the string function to draw both real numbers and
strings together (draw will only accept *either* a string *or* a real,
but not both).
