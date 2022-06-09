# fps

In GameMaker there are two main ways that can be used to tell the speed
at which your game runs. The [ game speed
](../General_Game_Control/game_get_speed) (as specified in the Game
Options) and the fps (frames per second). These values are often
confused, but basically one is the number of game steps that GameMaker
is supposed to be completing in a second, while the other (the fps) is
the number of CPU steps that GameMaker is actually completing in a
second *up to a maximum value of the room speed itself* . To get the
true fps, ie. the actual number of cpu steps per game step, use the [
fps_real ](fps_real) variable. This **read-only** variable returns
the current fps as an integer value. Please note that the function will
only update once every step of your game and so may appear to "jump"
from one value to another, but this is quite normal.

#### Syntax:

``` gml
fps
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if debug_mode
{
    draw_text(32, 32, "FPS = " + string(fps));
}
```

The above code will check to see if the game is in debug mode and if it
is it will display the current fps on the screen.
