# buffer_get_size

With this function you can get the size of the given buffer in bytes.

#### Syntax:

``` gml
buffer_get_size(buffer);
```

|          |                                                                                       |                                             |
|----------|---------------------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                                  | Description                                 |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The index of the buffer to get the size of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _size = buffer_get_size(player_data);
var _temp = buffer_create(_size, buffer_fixed, 0);
```

The above code will create a new buffer and store its index in the local
variable "\_temp", with size of this new buffer being the same as that
of the buffer indexed in the variable "player_data".
