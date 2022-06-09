# ds_map_secure_save_buffer

This function will save a previously created DS map to a buffer. You
supply the DS map ID value (as returned by the function [
ds_map_create() ](ds_map_create) ) and the ID of the buffer to write
to (as returned by the function [ buffer_create()
](../../Buffers/buffer_create) ). Note that if the DS map being
saved contains an array, this will be converted into a DS list instead
when saved. **IMPORTANT!** The secure saved DS map file can only be
loaded on the device that created it, and if you try to load a file that
was saved on a different device, then it will not work. **NOTE** : This
function is not supported on HTML5 and UWP.

#### Syntax:

``` gml
ds_map_secure_save_buffer(filename);
```

|          |                                                                                                          |                        |
|----------|----------------------------------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                                                     | Description            |
| id       |  [DS Map ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Maps/ds_map_create)  | The DS map ID value.   |
| buffer   |  [Buffer ID](../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                  | The buffer to save to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buff = buffer_create(128,buffer_grow,4);
var map = ds_map_create();
ds_map_add(map,"bob","ajob");
ds_map_add(map,"money",10);
ds_map_secure_save_buffer(map, buff);
ds_map_destroy(map);
```

The above code will create a buffer and a DS map, then populate the map
with some values and write it to the buffer before deleting the map.
