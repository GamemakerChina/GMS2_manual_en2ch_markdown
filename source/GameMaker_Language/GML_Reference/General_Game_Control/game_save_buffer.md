# game_save_buffer

This is a variant of the [game_save()](game_save) function, so
please read [its page](game_save) first as it contains important
information related to its use and to this function's as well. With this
function you can save the current state of the game to a previously
created "grow" buffer (see [Buffers](../Buffers/Buffers) ) which can
then be loaded again at any time using [ game_load_buffer()
](game_load_buffer) function. This function is designed for use in a
single room at a time (ie: it's not advised to do a buffer save in one
room, then try and load the buffer from another one) and should ideally
be used only for checkpoints or level restarts. **NOTE** : This function
is *very* limited and it is designed for the beginner to get a
checkpoint system up and running quickly, but more advanced users may
prefer to code their own system using the
[File](../File_Handling/File_Handling) functions, due to the fact
that the game will *not* save any of the dynamic resources like data
structures, surfaces, added sprites etc.

#### Syntax:

``` gml
game_save_buffer(buffer);
```

|          |                                                                                       |                           |
|----------|---------------------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                                  | Description               |
| buffer   |  [Buffer ID](../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)  | The buffer id to save to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("S"))
{
    global.Checkpoint = true;
    game_save_buffer(save_buff);
}
```

The above code will set a global variable to true and then save the
current game state to the buffer indexed in the variable "save_buff"
when the key "S" is pressed.
