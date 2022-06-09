# display_get_frequency

This function returns the frequency (or refresh rate) of the display
that the game is being played on. It will return a real value as
frames-per-second, so for example if your monitor is 60hz you will get
60 , if it's running at 144hz then you will get 144 , and so on. NOTE
This function is not supported on HTML5.

#### Syntax:

``` gml
display_get_frequency();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _freq = display_get_frequency();

if (_freq &amp;gt;= 240)
{
    game_set_speed(240, gamespeed_fps);
}
else if (_freq &amp;gt;= 120)
{
    game_set_speed(120, gamespeed_fps);
}
else if (_freq &amp;gt;= 60)
{
    game_set_speed(60, gamespeed_fps);
}
else
{
    game_set_speed(30, gamespeed_fps);
}
```

The above code gets the frequency of the display, and runs some
conditions to set the game running at 240, 120, 60 or 30 fps. This means
that if your display is 90hz the game will run at 60 fps, if it's 144hz
then it will run at 120 fps, etc. Of course, you can pass the frequency
of the display directly into
[game_set_speed()](../General_Game_Control/game_set_speed) so it's
used as the game's frame rate.
