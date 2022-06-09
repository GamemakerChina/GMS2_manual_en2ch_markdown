# buffer_save_ext

With this function you can save part of the contents of a buffer to a
file, ready to be read back into memory using the [ buffer_load()
](buffer_load) function. The "offset" defines the start position
within the buffer for saving (in bytes), and the "size" is the size of
the buffer area to be saved from that offset onwards (also in bytes).

#### Syntax:

``` gml
buffer_save_ext(buffer, filename, offset, size);
```

|          |                                                                                       |                                                       |
|----------|---------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                                  | Description                                           |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to save.                      |
| filename |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                 | The name of the file to save as.                      |
| offset   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The offset within the buffer to save from (in bytes). |
| size     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The size of the buffer area to save (in bytes).       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_save_ext(buff, "Player_Save.sav", 0, 16384);
```

Saves part of the current contents of the buffer with the id stored in
the variable "buff" to a file.
