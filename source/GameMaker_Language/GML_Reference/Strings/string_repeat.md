# string_repeat

This function simply returns the same string repeated a given number of
times over itself.

#### Syntax:

``` gml
string_repeat(str, count);
```

|          |                                                                        |                                           |
|----------|------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                   | Description                               |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to repeat.                     |
| count    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)    | The number of times to repeat the string. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = "Hello World"; str2 = string_repeat(str1, 3);
```

The above code will set str2 to "Hello WorldHello WorldHello World".
