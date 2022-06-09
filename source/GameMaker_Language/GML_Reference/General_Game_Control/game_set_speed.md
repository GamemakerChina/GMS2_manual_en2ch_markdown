# game_set_speed

This function can be used to set the game speed. You can set this in one
of two ways - as either game frames per second (FPS) or as microseconds
per game frame (MPF) - using one of the following two constants:

|                          |                                                   |
|--------------------------|---------------------------------------------------|
| Constant                 | Description                                       |
|  gamespeed_fps           | Sets the game speed using frames per second.      |
|  gamespeed_microseconds  | Sets the game speed using microseconds per frame. |

So, for example, a game speed of 30 frames per second would be 33333
microseconds per game game frame, which would then be expressed by this
function as either:

``` gml
game_set_speed(30, gamespeed_fps);
```

or:

``` gml
game_set_speed(33333, gamespeed_microseconds);
```

#### Syntax:

``` gml
game_set_speed(speed, type);
```

|          |                                                                                                               |                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                                                          | Description                                                              |
| speed    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | The new game speed (as either FPS or MPF).                               |
| type     |  [Game Speed Constant](../../../../GameMaker_Language/GML_Reference/General_Game_Control/game_get_speed)  | The type of method used to set the game speed (see the constants above). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if os_browser == browser_not_a_browser
{
    game_set_speed(60, gamespeed_fps);
}
else
{
    game_set_speed(30, gamespeed_fps);
}
```

The above code checks to see if the game is running in a browser and
sets the game speed accordingly as an FPS value.
