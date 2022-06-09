# uwp_show_help

This function launches the Xbox One help app which will in-turn display
your game's help file (which is an HTML format file that you have
previously uploaded to the XBox Developer Portal). Note that a user ID
is specified when calling this function so that the user's locale
information can be used when displaying it. You can retrieve the user ID
with the functions [ xboxlive_get_user()
](Users_And_Accounts/xboxlive_get_user) , [
xboxlive_get_activating_user()
](Users_And_Accounts/xboxlive_get_activating_user) , or [
uwp_license_trial_user() ](uwp_license_trial_user) .

#### Syntax:

``` gml
uwp_show_help(user_id);
```

|          |                                                                                                                           |                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                                                                      | Description                                   |
| user_id  |  [Xbox User ID](../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The User ID pointer to open the helpfile for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gamepad_button_check_pressed(0, gp_start)
{
    if uwp_license_trial_version()
    {
        var _uid = uwp_license_trial_user;
        uwp_show_help(_uid);
    }
}
```

The above code checks to see if a button is pressed and then checks the
app to see if it is running with a trial licence. If it is, then it gets
the User ID for licence and opens the help file for that user.
