# uwp_license_trial_user

This function will return the User ID pointer whose trial license is
currently being used, or it will return pointer_null if the user is not
currently active or if the game is not currently in trial mode.

#### Syntax:

``` gml
uwp_license_trial_user();
```

#### Returns:

``` gml
 Xbox User ID
```

#### Example:

``` gml
if gamepad_button_check_pressed(0, gp_start)
{
    if uwp_license_trial_version()
    {
        var _uid = uwp_license_trial_user();
        uwp_show_help(_uid);
    }
}
```

The above code checks to see if a button is pressed and then checks the
app to see if it is running with a trial licence. If it is, then it gets
the User ID for licence and opens the help file for that user.
