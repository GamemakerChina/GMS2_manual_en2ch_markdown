# window_set_max_height

This function can be used to set a maximum window height for your game.
If you enable the window resize option in the Game Options for the
target platform, then the player can resize the game window to any size
they wish, however by using this function you can limit the maximum
height to the size you specify. If you wish to go back to the default
behaviour (ie: no minimum), then use a value of -1. **NOTE** : This
function is only available on the **Windows** , **macOS** and **Linux**
platforms.

#### Syntax:

``` gml
window_set_max_height(height);
```

|          |                                                                         |                                                   |
|----------|-------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                    | Description                                       |
| height   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The maximum height in pixels for the game window. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
window_set_min_width(640); window_set_min_height(480);
 window_set_max_width(1280);
 window_set_max_height(960);
```

The above code will set the minimum and maximum width and height for the
game window.
