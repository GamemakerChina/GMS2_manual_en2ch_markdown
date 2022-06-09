# xboxlive_sponsor_for_user

This function retrieves the ID of the given user's sponsor.

#### Syntax:

``` gml
xboxlive_sponsor_for_user(user_id);
```

|          |                                                                                                                              |                                      |
|----------|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                                         | Description                          |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The ID pointer of the user to check. |

#### Returns:

``` gml
 Xbox Sponsor ID
```

#### Example:

``` gml
var _uid = xboxlive_user_for_pad(0);
sponsor = xboxlive_sponsor_for_user(_uid);
```

The above code gets the user ID pointer for the user assigned to the
gamepad \[0\] slot, and then uses that ID to retrieve the users sponsor
ID.
