# game_load

With this function you can load a game that has been previously saved
using [ game_save() ](game_save) . Note that it will restore the
version of the game that was used to create the save, so any updates
made after it will not be visible. For more info, read the page on [
game_save() ](game_save) .

#### Syntax:

``` gml
game_load(filename);
```

|          |                                                                        |                                    |
|----------|------------------------------------------------------------------------|------------------------------------|
| Argument | Type                                                                   | Description                        |
| filename |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to load from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("L"))
{
    if (global.Save) game_load("Save.dat");
}
```

The above code will load a previously saved game if a global variable is
true when the player presses the "L" key.
