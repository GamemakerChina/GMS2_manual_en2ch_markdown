# fps_real

In GameMaker there are two main ways that can be used to tell the speed
at which your game runs. The [ game speed
](../General_Game_Control/game_get_speed) (as specified in the Game
Options) and the fps (frames per second). These values are often
confused, but basically one is the number of game steps that GameMaker
is supposed to be completing in a second (game speed), while the other
is the number of CPU steps that GameMaker is actually completing in a
second (the real fps), and this value is generally much higher than the
game speed, but will drop as your game gets more complex and uses more
processing power to maintain the set room speed. This **read-only**
variable returns the current fps as an integer value. Please note that
the function will only update once every step of your game and so may
appear to "jump" from one value to another, but this is quite normal.
**NOTE** : On the HTML5 target, this variable will instead return a
multiple of the monitor refresh rate as GameMaker has to rely on the
browser for timing and despatch.

#### Syntax:

``` gml
fps_real
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if debug_mode
{
    draw_text(32, 32, "FPS = " + string(fps_real));
}
```

The above code will check to see if the game is in debug mode and if it
is it will display the current real fps on the screen.
