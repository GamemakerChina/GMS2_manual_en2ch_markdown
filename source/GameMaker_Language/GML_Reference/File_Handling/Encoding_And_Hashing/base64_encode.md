# base64_encode

This function will convert a string into a base64 format encoded string.
This is a commonly used encoding scheme that is often used for any media
that needs to be stored or transferred over the internet as text, and
renders the output unreadable to the human eye.

#### Syntax:

``` gml
base64_encode(string)
```

|          |                                                                           |                       |
|----------|---------------------------------------------------------------------------|-----------------------|
| Argument | Type                                                                      | Description           |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to encode. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var str, file; str = base64_encode(game_data); file = file_text_open_write("save.txt"); file_text_write_string(file, str); file_text_close(file);
```

The above code will covert the string stored in "game_data" into a
base64 encoded string which is then stored in an external text file.
