# uwp_is_suspending

This function will return true for a single frame (and false otherwise)
in a similar manner to [ os_is_paused()
](../OS_And_Compiler/os_is_paused) . The game then has one second to
save the game state before it is potentially terminated by the system.
Once the game has finished saving data it should call [ uwp_suspend()
](uwp_suspend) to suspend cleanly. The game should probably also
enter a pause state so that if it is resumed by the system (if it hasn't
been fully terminated) the player is not thrown straight back into a
gameplay situation.

#### Syntax:

``` gml
uwp_is_suspending();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if uwp_is_suspending()
{
    scr_Save_Game_Data();
    uwp_suspend();
}
```

The above code checks to see if the app is going into suspension and if
it is it calls a script to save the game data before suspending the
game.
