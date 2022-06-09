# Built-In Time Sources

|                                                                                                               |                          |       |
|---------------------------------------------------------------------------------------------------------------|--------------------------|-------|
|  [Time Source Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Built_In_Time_Sources)  |                          |       |
| Constant                                                                                                      | Description              | Value |
|  time_source_global                                                                                           | The Global Time Source   | 0     |
|  time_source_game                                                                                             | The Game Time Source     | 1     |

You can use the **Global Time Source ** or the **Game Time Source ** as
a parent for your custom Time Source . Both Time Source s are globally
available. The Global Time Source runs outside the main game loop, while
the Game Time Source runs as part of the game loop. The choice between
Global/Game doesn't affect whether Time Source s are affected by your
game's framerate; that will depend on the [unit](Time_Source_Units)
you use.

## Order

Time Source s inheriting from the Global Time Source are processed
**before** the Game Time Source .

## States

The Game Time Source has [states](Time_Source_States) , meaning it
can be [paused](time_source_pause) . The Global Time Source doesn't
have states and can't be paused. You can use the Global Time Source for
timers that should run regardless of the game state, and the Game Time
Source for timers that are tied to your main game loop. You can then
pause all of your game-related timers by pausing the Game Time Source .
