# xboxlive_user_is_signed_in

The function will check to see if a user is signed-in and return true if
there is and false otherwise. If no user is signed in then you can call
the function [ xboxlive_show_account_picker()
](xboxlive_show_account_picker) to open the account picker and
prompt them to sign-in.

#### Syntax:

``` gml
xboxlive_user_is_signed_in();
```

#### Returns:

``` gml
 Boolean
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
