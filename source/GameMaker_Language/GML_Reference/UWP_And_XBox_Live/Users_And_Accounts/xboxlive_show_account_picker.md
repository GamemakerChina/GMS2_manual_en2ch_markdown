# xboxlive_show_account_picker

The function will open the XBox Account Picker screen so that the user
can sign-in if they are not already signed in (if they are then the
function will do nothing). Note that this function is only applicable
when using the UWP build on PC and not Xbox, as to launch a game on Xbox
the user has to have signed in already.

#### Syntax:

``` gml
xboxlive_show_account_picker();
```

#### Returns:

``` gml
N/A
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
