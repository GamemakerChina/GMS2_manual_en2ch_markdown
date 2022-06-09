# string_lower

With this function you can force a string to contain only lower case
characters. NOTE This function only detects the 26 letter English
alphabet from A - Z.

#### Syntax:

``` gml
string_lower(string);
```

|          |                                                                        |                                     |
|----------|------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                   | Description                         |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to convert to lowercase. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = "Hello World"; str2 = string_lower(str1);
```

The above code will set str2 to "hello world".
