# window_set_position

With this function you can set the game window to a specific position
within the display (on macOS, Linux(Ubuntu) and Windows) or within the
browser (HTML5). **NOTE** : If your HTML5 game uses a custom indexl
and that sets the canvas to a fixed position then this function will
have no effect on the window position.

#### Syntax:

``` gml
window_set_position(x, y);
```

|          |                                                                         |                                                   |
|----------|-------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                    | Description                                       |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of where to position the window. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of where to position the window. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
window_set_position(0, 0);
```

The above code will position the game window in the upper left corner of
the browser or display (depending on the target module being used).
