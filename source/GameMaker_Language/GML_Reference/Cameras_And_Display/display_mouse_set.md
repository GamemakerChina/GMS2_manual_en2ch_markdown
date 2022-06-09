# display_mouse_set

With this function you can change or set the position of the mouse
within the game display which can be useful for FPS games, for example.
The function will only work while the game is in focus and using ALT +
Tab will unlock the mouse. NOTE This function is only usable on Desktop
platforms (i.e. Windows, Mac and Ubuntu).

#### Syntax:

``` gml
display_mouse_set(x, y);
```

|          |                                                                      |                                  |
|----------|----------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                 | Description                      |
| x        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate in the display. |
| y        |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate in the display. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
display_mouse_set(display_get_width() / 2, display_get_height() / 2);
```

The above code would center the mouse in the game display.
