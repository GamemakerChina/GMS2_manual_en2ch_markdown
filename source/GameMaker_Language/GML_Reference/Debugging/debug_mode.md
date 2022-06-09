# debug_mode

This **read only** variable returns true when the game is being played
in debug mode and false when being played as normal.

#### Syntax:

``` gml
debug_mode
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if debug_mode
{
    ini_open("Cheats.ini");
}
else
{
    ini_open("Game.ini");
}
```

The above code opens a different ini file depending on the value of the
read-only variable debug_mode .
