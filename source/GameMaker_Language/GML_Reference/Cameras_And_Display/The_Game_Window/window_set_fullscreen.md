# window_set_fullscreen

With this function you can set the game window to be full screen ( true
) or not ( false ). Please note that for the **macOS** target, you
*must* have unchecked the "Start In Fullscreen" option and checked the
"Allow the player to resize the game window" option in the [Game
Options](../../../../Settings/Game_Options) , otherwise this
function will fail. Also note that this function will *not* work on
HTML5 unless it's added in as a "clickable" callback (see
[here](../../Web_And_HTML5/clickable_add) for more details).

#### Syntax:

``` gml
window_set_fullscreen(full);
```

|          |                                                                            |                                                                |
|----------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                    |
| full     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to set the screen to fullscreen (true) or not (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    if window_get_fullscreen()
    {
        window_set_fullscreen(false);
    }
    else
    {
        window_set_fullscreen(true);
    }
}
```

The above code checks for a mouse button press and then sets the window
to fullscreen if it is not already, or sets it to windowed if it is
already.
