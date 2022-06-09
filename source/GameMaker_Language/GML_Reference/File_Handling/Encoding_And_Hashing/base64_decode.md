# base64_decode

This function will convert a string encoded previously using base64
format, into standard text. Base64 is a commonly used encoding scheme
that is often used for any media that needs to be stored or transferred
over the internet as text, and renders the output unreadable to the
human eye.

#### Syntax:

``` gml
base64_decode(string)
```

|          |                                                                           |                       |
|----------|---------------------------------------------------------------------------|-----------------------|
| Argument | Type                                                                      | Description           |
| string   |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The string to decode. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var str, file; str = base64_encode(game_data); file = file_text_open_read("save.txt"); str = file_text_read_string(file); level_data = base64_decode(str); file_text_close(file);
```

The above code will open a text file and read a string from it into the
local variable "str". This string is then decoded and the result stored
in the instance variable "level_data".
