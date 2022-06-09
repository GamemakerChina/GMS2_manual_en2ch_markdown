# window_set_rectangle

With this function you can set the position of the game window within
the browser (HTML5) or display (Windows, Ubuntu (Linux) or macOS) *and*
set the scale of the window too. For more information on window position
and window size, see [ window_set_position()
](../The_Game_Window/window_set_position) and [ window_set_size()
](../The_Game_Window/window_set_size) .

#### Syntax:

``` gml
window_set_rectangle(x, y, w, h);
```

|          |                                                                         |                                     |
|----------|-------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                    | Description                         |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new x coordinate of the window. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new y coordinate of the window. |
| w        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new width of the window.        |
| h        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The new height of the window.       |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
window_set_rectangle(0, 0, display_get_width(), display_get_height());
```

The above code will set the game window to occupy the whole display area
(either the browser or the screen, depending on the target platform).
