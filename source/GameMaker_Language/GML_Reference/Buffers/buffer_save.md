# buffer_save

With this function you can save the contents of a buffer to a file,
ready to be read back into memory using the [ buffer_load()
](buffer_load) function. **NOTE** : On HTML5 the contents of the
buffer will be saved as base64 encoded strings when using this function.

#### Syntax:

``` gml
buffer_save(buffer, filename);
```

|          |                                                                                       |                                  |
|----------|---------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                  | Description                      |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to save. |
| filename |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                 | The name of the file to save as. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buffer_save(buff, "Player_Save.sav");
```

Saves the current contents of the buffer with the id stored in the
variable "buff" to a file.
