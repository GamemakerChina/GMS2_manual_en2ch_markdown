# show_error

This function will show a custom string as an error message. IMPORTANT
The second argument only exists for backwards compatibility with older
projects and will have no effect on the error dialog shown. **NOTE**
This function is for debug use **only** .

#### Syntax:

``` gml
show_error(str, abort);
```

|          |                                                                         |                                                                                                   |
|----------|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                                       |
| str      |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)   | The string to show in the pop-up message.                                                         |
| abort    |  [Boolean](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  UNUSED Whether the error should abort the game (true) or allow the player to ignore it (false).  |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (room != rm_Dungeon)
{
    show_error("Error: Went to wrong area. Aborting game.", true);
}
```

The above code will check if the current room is rm_Dungeon , and if
it's not, it will show an error message.
