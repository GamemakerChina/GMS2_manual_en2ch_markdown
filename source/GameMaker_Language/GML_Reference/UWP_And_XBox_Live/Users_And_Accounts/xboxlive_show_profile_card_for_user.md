# xboxlive_show_profile_card_for_user

With this function you can request that the XBox shows the profile card
for the target user ID pointer. The function requires both the user ID
pointer for the user that is *requesting* the information as well as the
user ID pointer of the user to *target* and get the profile card of.

#### Syntax:

``` gml
xboxlive_show_profile_card_for_user(requesting_user_id, target_user_id);
```

|                    |                                                                                                                              |                                                                |
|--------------------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument           | Type                                                                                                                         | Description                                                    |
| requesting_user_id |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID (a pointer) of the requesting user                 |
| target_user_id     |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID (a pointer) of the user to get the profile card of |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (gamepad(0, gp_start))
{
    xboxlive_show_profile_card_for_user(user[0], user[1]);
}
```

The above code checks for a gamepad button press and if one is detected
it shows the profile card for the given user.
