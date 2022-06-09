# buffer_load_partial

This function will load some of the buffer data that was previously
saved using the [ buffer_save() ](buffer_save) functions into an
existing buffer. You give the id of the previously created buffer to
load into, then the saved buffer file to load, and then the offset from
the start of the buffer (in bytes) that you wish to load the data from.
The following arguments are for setting the length of the buffer data
(in bytes) from the initial offset point that you wish to load and the
offset point to load the data to in the buffer (again, in bytes). Please
read the [buffer_load()](buffer_load) page for platform-specific
notes.

#### Syntax:

``` gml
buffer_load_partial(buffer, filename, offset, src_len, dest_offset);
```

|             |                                                                                       |                                                                                          |
|-------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Argument    | Type                                                                                  | Description                                                                              |
| buffer      |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to load into (destination).                                      |
| filename    |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                 | The name of the file to load from (source).                                              |
| offset      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The offset within the destination buffer to load to (in bytes).                          |
| src_len     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The length of the part of the source buffer to load (in bytes).                          |
| dest_offset |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                   | The offset where to start putting the partial data in the destination buffer (in bytes). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
buff = buffer_create(256, buffer_grow, 1);
var _file = "save.dat";
var _so = 6;
var _sl = 5;
var _do= 0;
buffer_load_partial(buff, _file, _so, _sl, _do);
```

The above code will create a new "grow" buffer and then load in a part
of the data saved in the file "save.dat" to it.
