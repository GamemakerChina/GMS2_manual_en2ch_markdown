# uwp_suspend

This function indicates to the system that the app has finished saving
data following detection of a suspension request. Calling this function
is a requirement for Xbox One submission, and it should always be used
in conjunction with the function [ uwp_is_suspending()
](uwp_is_suspending) , as shown in the example below.

#### Syntax:

``` gml
uwp_suspend();
```

#### Returns:

``` gml
N/A
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
