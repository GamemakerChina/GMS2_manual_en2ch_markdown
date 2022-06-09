# cloud_file_save

This function will commit a file to the chosen cloud service for
storage. The function will return a unique **id** value that should then
be used in the appropriate asynchronous event to identify the DS map
that is returned as a "call back" from the cloud service. The file
should contain *all* the information that you need to save for your game
as you can only store one single "data blob" to the cloud, and running
this function again will overwrite any previously stored values (as will
using the [ cloud_string_save() ](cloud_string_save) function). The
description should be a short string of information that describes the
save, eg: "Level2, Stage2". For further information on the returned
asynchronous data, please see the function [ cloud_synchronise()
](cloud_synchronise) .

#### Syntax:

``` gml
cloud_file_save(file, description);
```

|             |                                                                           |                                               |
|-------------|---------------------------------------------------------------------------|-----------------------------------------------|
| Argument    | Type                                                                      | Description                                   |
| string      |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The file to be uploaded (as a string).        |
| description |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | A brief description of the data being stored. |

#### Returns:

``` gml
 Async Request ID
```

#### Example:

``` gml
var t_str = "";
for (var i = 0; i &amp;lt; 10; i++;)
{
    t_str += string(global.Highscore[i]) + "|"
}
var file = file_text_open_write("Highscores.txt");
file_text_write_string(file, t_str);
file_text_close(file);
save_check = cloud_file_save("Highscores.txt", "Current Highscores");
```

The above code creates a string from the values stored in the global
array "Highscores" and then writes this string to a file for local
storage. The file is then sent to the cloud service for storage.
