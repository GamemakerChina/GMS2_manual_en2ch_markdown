# game_restart

With this function you can restart the game. This is essentially the
same as running the game for the first time and so the [Game Start
Event](../../../The_Asset_Editors/Object_Properties/Other_Events)
will be triggered, *as well as* the [Game End
Event](../../../The_Asset_Editors/Object_Properties/Other_Events) .
NOTE You will not be able to create new instances in the same event
after this function has been called. It should be noted that certain
things will **not** be reset when this function is called:

-   Global variables will not be re-initialised unless explicitly coded
    as such - for example, the built-in global variable score will not
    start at zero after a game restart if it has been modified in the
    game already.
-   The GPU state will not be changed (so if you have set the draw
    colour or alpha, for example, it will remain at the changed value).
-   The game speed will remain at whatever you set it in your game code
    (if you changed it this change will be perpetuated).
-   Any asset from the Asset Browser that has been changed at run time
    within the game - for example if you change the origin for a sprite
    resource or shift the position of a path resource - will *not* be
    reset.
-   Dynamic resources like buffers, surfaces, data-structures or
    imported sprites will also not be cleaned up or removed (although
    you may lose references to them, so take care when using this
    function to either use global references for the dynamic resource,
    or to clean them up before the function is called).

#### Syntax:

``` gml
game_restart();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("R")) game_restart();
```

This would restart the game when the player presses the "R" key.
