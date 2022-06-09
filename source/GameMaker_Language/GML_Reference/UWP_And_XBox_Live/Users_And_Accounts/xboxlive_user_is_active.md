# xboxlive_user_is_active

With this function you can check whether the given user ID is in the
list of users currently using the console, and the function will return
true if they are, or false otherwise. You can get a User ID pointer with
the function [xboxlive_get_user()](xboxlive_get_user) .

#### Syntax:

``` gml
xboxlive_user_is_active(user_id);
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
        global.Player_ID[global.PlayerNum++] = _uid;
    }
}
```

The above code loops through the user accounts and then checks to see if
any of them are active. If they are, their user ID is added into a
global array.
