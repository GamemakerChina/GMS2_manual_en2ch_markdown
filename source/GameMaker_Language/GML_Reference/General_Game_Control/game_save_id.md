# game_save_id

This **read-only** variable will return the full path ID of the
directory that is used by your game to save files to. This directory may
or may not be visible to other applications, depending on the platform.
On the HTML5 target it will return an empty string. NOTE This variable
exists purely for information and should **not** be used to get a file
path or anything similar, as it will not work correctly across all
platforms.

#### Syntax:

``` gml
game_save_id
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
save_dir = game_save_id;
```

This will store the directory for saving files to a variable for future
use.
