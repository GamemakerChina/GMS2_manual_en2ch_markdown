# game_project_name

This **read only** variable returns the display name of your game for
the target platform in a "save-friendly" format for the target platform.
If the display name contains any characters that are not permitted for a
file name, they will be replaced automatically with "\_". The display
name can be set in the [Game
Options](../../../Settings/Game_Options) . Note that since there are
no restrictions on file names for HTML5, this string will probably be
the same as that returned by [ game_display_name
](game_display_name) .

#### Syntax:

``` gml
game_project_name
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var file = game_project_name + ".ini"; ini_open(file);
 ini_write_real("Scores", "Highscore", score); ini_close();
```

The above code gets the project name and uses this to open (or create)
an ini file which is then written to.
