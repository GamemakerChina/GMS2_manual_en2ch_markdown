# string_count

This function will return the amount of times the given substring
appears within a specific string. In this way you can check for how many
times a single letter or a phrase is repeated in a section of stored
text.

#### Syntax:

``` gml
string_count(substr, str);
```

|          |                                                                        |                                        |
|----------|------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                   | Description                            |
| substr   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The substring to check the string for. |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to check.                   |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
str1 = "Hello World"; ocount = string_count( "o", str1 );
```

This will set the variable ocount to the number of "o"s in str1 , in
this case 2.
