# ds_map_secure_load_buffer

This function will load a secure saved DS map from a buffer. You must
previously have loaded the buffer into memory (using [ buffer_load()
](../../Buffers/buffer_load) ) and then passing that into this
function will return a DS map populated with the contents of the buffer.
Note that the buffer must have been created using the function
[ds_map_secure_save_buffer()](ds_map_secure_save_buffer) for this to
work correctly, and also note that if the DS map being loaded contained
an array, this will be converted into a DS list instead on load.
**IMPORTANT!** One of the features of a secure saved file is that it is
locked to the device that it was created on, so you cannot load a file
saved on one device into a project running on another device. **NOTE** :
This function is not supported on HTML5 and UWP.

#### Syntax:

``` gml
ds_map_secure_load_buffer(buffer);
```

|          |                                                                                          |                                                        |
|----------|------------------------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                                     | Description                                            |
| buffer   |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The buffer ID of the buffer to load the map data from. |

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
var buff = buffer_load("save.dat");
map = ds_map_secure_load_buffer(buff);
buffer_delete(buff);
```

The above code will load a securely saved DS map from a buffer and store
its index value in a variable for future use.
