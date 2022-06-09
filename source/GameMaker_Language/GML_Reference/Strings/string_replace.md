# string_replace

You can use this function to parse a string looking for a specific part,
which can then be replaced by the new string that you have specified.

#### Syntax:

``` gml
string_replace(str, substr, newstr);
```

|          |                                                                        |                                                 |
|----------|------------------------------------------------------------------------|-------------------------------------------------|
| Argument | Type                                                                   | Description                                     |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to be copied.                        |
| substr   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The substring within the string to be replaced. |
| newstr   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new substring to replace the previous one.  |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str1 = "Hello Earth"; str2 = string_replace(str1, "Earth", "World");
```

This will set str2 to str1 , but with its instance of "Earth" replaced
with "World", resulting in str2 being "Hello World".
