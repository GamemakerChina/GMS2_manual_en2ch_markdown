# window_mouse_set

With this function you can change or set the position of the mouse
within the game window which can be useful for FPS games, for example.
The function will only work while the game is in focus and using alt +
tab will unlock the mouse. NOTE This function is only usable on Desktop
platforms (i.e. Windows, Mac and Ubuntu). **NOTE** For regular mouse
functions see the section on [Mouse
Input](../../Game_Input/Mouse_Input/Mouse_Input) .

#### Syntax:

``` gml
window_mouse_set(x, y);
```

|          |                                                                         |                                 |
|----------|-------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                    | Description                     |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate in the window. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate in the window. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
window_mouse_set(window_get_width() / 2, window_get_height() / 2);
```

The above code would center the mouse in the game window.
