# game_load_buffer

With this function you can load a game state that has been saved
previously. The game is loaded from a previously created "grow" buffer
(see [Buffers](../Buffers/Buffers) ) and the buffer must have had a
game state saved to it using [ game_save_buffer()
](game_save_buffer) function.

#### Syntax:

``` gml
game_load_buffer(buffer);
```

|          |                                                                                       |                             |
|----------|---------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                  | Description                 |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The buffer id to load from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("L"))
{
    if global.Checkpoint game_load_buffer(save_buff);
}
```

The above code will load a previously saved game state from the buffer
indexed in the variable "save_buff", only if the global variable is true
, when the player presses the "L" key.
