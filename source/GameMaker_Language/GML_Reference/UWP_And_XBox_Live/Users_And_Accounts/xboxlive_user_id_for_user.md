# xboxlive_user_id_for_user

This function converts the User ID pointer into a string.

#### Syntax:

``` gml
xboxlive_user_id_for_user(user_id);
```

|          |                                                                                                                              |                                      |
|----------|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                                         | Description                          |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The ID pointer of the user to check. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var _uid = xboxlive_user_for_pad(0); uid_string = xboxlive_user_id_for_user(_uid);
```

The above code gets the user ID pointer for the user assigned to the
gamepad \[0\] slot, and then saves that user ID as a string to an
instance variable.
