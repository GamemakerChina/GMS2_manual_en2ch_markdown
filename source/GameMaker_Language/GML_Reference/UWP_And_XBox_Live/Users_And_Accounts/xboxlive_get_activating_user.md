# xboxlive_get_activating_user

With this function you can retrieve the user ID pointer for the user
that launched the game from the console. **NOTE** : How you use this
pointer will depend on what you want to do in the game, but you should
not rely on it to be the currently playing User ID as the activating
user can logout while the game is running.

#### Syntax:

``` gml
xboxlive_get_activating_user();
```

#### Returns:

``` gml
 Xbox User ID
```

#### Example:

``` gml
global.activUser = xboxlive_get_activating_user();
```

The above stores the activating user ID pointer in a global variable
