# xboxlive_user_is_remote

This function will check the given user ID and return true if the player
is a remote player, or false otherwise.

#### Syntax:

``` gml
xboxlive_user_is_remote(user_id);
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
global.PlayerNum = 0;
global.Player_ID = array_create();
for(var i = 0; i &amp;lt; xboxlive_get_user_count(); ++i;)
{
    var _uid = xboxlive_get_user(i);
    if xboxlive_user_is_active(_uid)
    {
        if !xboxlive_user_is_remote(_uid)
        {
            global.Remote_Player_ID[global.PlayerNum++] = _uid;
        }
    }
}
```

The above code loops through the user accounts and then checks to see if
any of them are active. If they are, their user ID is added into a
global array, only if they are not remote users.
