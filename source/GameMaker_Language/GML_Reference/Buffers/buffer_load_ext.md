# buffer_load_ext

This function will load the buffer data that was previously saved using
the [ buffer_save() ](buffer_save) functions into an existing
buffer. You give the ID of the previously created buffer to load into,
then the saved buffer file to load, and finally the offset from the
start of the buffer (in bytes) that you wish to load the data to. Please
read the [buffer_load()](buffer_load) page for platform-specific
notes.

#### Syntax:

``` gml
buffer_load_ext(buffer, filename, offset);
```

|          |                                                                                       |                                                     |
|----------|---------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                  | Description                                         |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to load into.               |
| filename |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                 | The name of the file to load from.                  |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The offset within the buffer to load to (in bytes). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var pos = buffer_seek(player_buffer, buffer_seek_end, 0);
buffer_load(player_buffer, "Data_Save.sav", pos);
```

The above code will first get the position of the end of the buffer
indexed in the variable "player_buffer" and then loads the data from the
given into that position (note that this example will only work with
"grow" or "wrap" buffer types).
