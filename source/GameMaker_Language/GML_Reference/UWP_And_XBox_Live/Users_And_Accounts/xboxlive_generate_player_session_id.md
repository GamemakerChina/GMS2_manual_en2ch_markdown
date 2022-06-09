# xboxlive_generate_player_session_id

This function will generate a unique string (containing a GUID) for the
current player session. This can then be used with the function [
xboxlive_fire_event()
](../Stats_And_Leaderboards/xboxlive_fire_event) .

#### Syntax:

``` gml
xboxlive_generate_player_session_id();
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if !xboxlive_user_is_signed_in()
{
    if !xboxlive_user_is_signing_in()
    {
        xboxlive_show_account_picker();
    }
}
else
{
    global.GamerTag = xboxlive_gamertag_for_user();
}
```

The above code checks to see if a user is signed-in to XBox Live and if
they are signed-in, the code will get the gamertag for the user and
store it in a global variable for future use. If they are not signed-in
then the code checks to see if they are in the process of signing-in, in
which case nothing further will happen, and if they are not, then it
will open the account picker, prompting them to sign-in.
