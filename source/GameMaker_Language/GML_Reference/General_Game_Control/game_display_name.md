# game_display_name

This **read only** variable returns the display name of your game for
the target platform, as set in the [Game
Options](../../../Settings/Game_Options) .

#### Syntax:

``` gml
game_display_name
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var name = game_display_name; var ver = string(GM_version); draw_text(32, 32, name + ":" + ver);
```

The above code gets the display name and the version number of the game
and draws them.
