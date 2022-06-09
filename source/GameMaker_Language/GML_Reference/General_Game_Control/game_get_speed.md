# game_get_speed

This function can be used to get the game speed as either the number of
game frames to run per second or as the number of micro seconds per game
frame. Note that this is **not** the actual running speed FPS value (for
that use the [ fps_real ](../Debugging/fps_real) variable) but
rather the number of game frames (FPS) that the game will attempt to
maintain each second, or the length of each game frame in microseconds
that the game will try to maintain (MPF). When you use this function you
need to give one of the following constants which will determine the
type of the return value:

|                                                                                                               |                                                   |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
|  [Game Speed Constant](../../../../GameMaker_Language/GML_Reference/General_Game_Control/game_get_speed)  |                                                   |
| Constant                                                                                                      | Description                                       |
|  gamespeed_fps                                                                                                | Gets the game speed using frames per second.      |
|  gamespeed_microseconds                                                                                       | Gets the game speed using microseconds per frame. |

So, for example, if the game speed is set at 30 in the Game Options and
you use the FPS type, then the function will return 30, but if you use
the MPF then the function will return 33333.

#### Syntax:

``` gml
game_get_speed(type);
```

|          |                                                                                                               |                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Argument | Type                                                                                                          | Description                                                              |
| type     |  [Game Speed Constant](../../../../GameMaker_Language/GML_Reference/General_Game_Control/game_get_speed)  | The type of method used to get the game speed (see the constants above). |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if game_get_speed(gamespeed_fps) != 60
{
    game_set_speed(60, gamespeed_fps);
}
```

The above code checks to see if the game is running with a game speed of
60 FPS and if not it is set to 60 FPS.
