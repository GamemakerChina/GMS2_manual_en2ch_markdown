# game_save

This is a legacy function that can be used to save the current state of
the game, and is not recommended for use anymore. Use the [File
functions](../File_Handling/File_Handling) instead to create a
custom save system where you only save and load specific game data. This
function will save the game's state as it is, however it will not save
any dynamic resources being used at that time, such as data structures,
surfaces, assets added at runtime, etc. If such a save file is loaded,
any game updates that were made after the save will not be visible, as
it will restore the version of the game that was used to create the
save. Note that save files created using this function may not be
supported by updated Runtime versions, so replacing this function with a
new save system is essential to ensure compatibility with future
GameMaker updates, and for the reasons listed above, updates made to
your own game.

#### Syntax:

``` gml
game_save(filename);
```

|          |                                                                        |                                           |
|----------|------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                   | Description                               |
| filename |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name of the file to save the game to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("S"))
{
    global.Saved = true;
    game_save("Save.dat");
}
```

The above code will set a global variable to true and then save the game
to the file "Save.dat" when the key "S" is pressed.
