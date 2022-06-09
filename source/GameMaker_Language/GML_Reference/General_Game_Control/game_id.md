# game_id  DEPRECATED 

This **read only** variable returns the unique identifier for the game
you have created. You can use this if you need a unique file name, or
anything else that needs something to identify your game only. This can
be set in the [Game Options](../../../Settings/Game_Options) .

#### Syntax:

``` gml
game_id
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
ini_open("Score.ini");
ini_write_real("Scores", "0", score + game_id);
ini_close();
```

The above code performs a very basic encryption on the score by adding
the game_id to it before saving. On reading it back into the game you
would deduct the game_id to get the correct value again.
