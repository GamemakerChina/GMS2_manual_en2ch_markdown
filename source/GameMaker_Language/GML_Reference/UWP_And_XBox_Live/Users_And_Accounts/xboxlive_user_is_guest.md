# xboxlive_user_is_guest

This function will return true if the given user ID pointer is a guest
user and false if they are not. You can get a User ID pointer with the
function [ xboxlive_get_user() ](xboxlive_get_user) .

#### Syntax:

``` gml
xboxlive_user_is_guest(user_id);
```

|          |                                                                                                                              |                                      |
|----------|------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| Argument | Type                                                                                                                         | Description                          |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The ID pointer of the user to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if xboxlive_user_is_guest(user_id[0])
{
    global.user_name[0] = "GUEST";
}
else
{
    global.user_name[0] = xboxlive_gamedisplayname_for_user(user_id[0]);
}
```

The above stores the activating user ID pointer in a global variable.
