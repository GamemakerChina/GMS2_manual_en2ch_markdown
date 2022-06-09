# game_end

With this function you can end the game (and the [Game End
Event](../../../The_Asset_Editors/Object_Properties/Other_Events)
will be triggered). This will not happen instantaneously, but rather at
the end of the current step, so any code you have in the same step after
this function has been called will still run. Please note that this
function has the following restrictions:

-   On Android devices, calling game_end() will push the app into the
    background, but it will *not* close the app. This must be done by
    the user.
-   On iOS it will do nothing and silently fail.
-   On all consoles (including UWP when running on an Xbox) it may crash
    the game or at best fail silently, and it may also be a submission
    fail, so this function *must not be used* .
-   On HTML5 it will end the game, but leave the user staring at a blank
    draw canvas on the web page, and as such it isn't recommended that
    it be used on that target platform.
-   On Windows (including UWP on a PC), Linux and macOS the function
    simply ends the game and closes the game window (the [Game End
    Event](../../../The_Asset_Editors/Object_Properties/Other_Events)
    will also be triggered).

#### Syntax:

``` gml
game_end();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(vk_escape) game_end();
```

This would end the game if the player presses the "escape" key.
