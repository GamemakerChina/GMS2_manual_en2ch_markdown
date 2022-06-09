# string_hash_to_newline

This function returns a string where the "#" symbol has been converted
into a new line. So a string formatted as:

``` gml
"Hello#World"
```

Would be printed to the screen as:

``` gml
Hello World
```

**IMPORTANT!** This function is provided for import compatibility
between GameMaker and previous versions of the software and as such this
function should not be used except when necessary to replicate obsolete
functionality. Instead you should be using the [escape
characters](Strings) to mark a new line. For more information on
import compatibility see
[here](../../../Additional_Information/Obsolete_Functions) .

#### Syntax:

``` gml
string_hash_to_newline(string);
```

|          |                                                                        |                                           |
|----------|------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                   | Description                               |
| string   |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to convert over multiple lines |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var str = string_hash_to_newline("Hello#World"); draw_text(32, 32, str);
```

The above code converts the string with the hash symbol into a string
split over two lines then prints it to the screen.
