# xboxlive_reputation_for_user

With this function you can retrieve the Xbox Live reputation score for
the given user ID pointer.

#### Syntax:

``` gml
xboxlive_reputation_for_user(requesting_user_id);
```

|                    |                                                                                                                              |                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument           | Type                                                                                                                         | Description                                  |
| requesting_user_id |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID (a pointer) of the user to check |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _a = 0;
var _num = xboxlive_get_user_count();
for (var i = 0; i &amp;lt; _num; ++i;)
{
    var _uid = xboxlive_get_user(i);
    if _uid != pointer_null
    {
        global.UserName[_a] = xboxlive_gamedisplayname_for_user(_uid);
        global.UserScore[_a] = xboxlive_gamerscore_for_user(_uid);
        global.UserRep[_a] = xboxlive_reputation_for_user(_uid);
        global.UserAvatar[_a] = xboxlive_sprite_add_from_gamerpicture(_uid, 256, 0, 0);
        ++a;
    }
}
```

The above code loops through the logged in users and stores their gamer
data in various global arrays.
