# GM_version

This constant hold the version number as defined in the [Game
Options](../../../Settings/Game_Options) for each target platform.
The value is stored as a string.

#### Syntax:

``` gml
GM_version;
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
draw_text(32, 32, date_time_string(GM_build_date)); draw_text(32, 64, "v" + GM_version);
```

The above code takes the GM date and version constants and draws them to
the screen.
