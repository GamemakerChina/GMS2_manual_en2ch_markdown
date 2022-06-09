# uwp_is_constrained

This function will return true if the game is running in a resource
constrained mode or false if running normally. Resource constrained mode
can be activated when the game doesn't have focus, and in this mode the
game has reduced GPU resources. The response to this should normally be
to pause the game (as the user no longer has control). Also, disabling
any particularly taxing effects may be a good idea if slowdown is
observed in this mode. Note that unlike the [ uwp_is_suspending()
](uwp_is_suspending) function, this function will return true
continuously as long as the game is in constrained mode (and not just
once when it first happens).

#### Syntax:

``` gml
uwp_is_constrained();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if xboxliveis_constrained()
{
    if !instance_exists(obj_PauseMenu)
    {
        instance_create(0,0,obj_PauseMenu);
    }
}
```

The above code checks to see if the app is constrained and if it is it
creates an instance of an object (used for pausing the game).
