# string_upper

With this function you can force a string to contain only upper case
characters. NOTE This function only detects the 26 letter English
alphabet from A - Z.

#### Syntax:

``` gml
string_upper(string);
```

|          |                                                                        |                                     |
|----------|------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                   | Description                         |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to convert to uppercase. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = "Hello World"; str2 = string_upper(str1);
```

The above code will set the variable str2 to "HELLO WORLD".
