# xboxlive_gamedisplayname_for_user

With this function you can retrieve the display name - as a string -
from the user ID pointer given. Note that if the user is local then the
returned value is simply a string of the their display name, but if it
is a remote user then the string will be their gamertag which can then
be used, for example, for muting/unmuting in voice chat.

#### Syntax:

``` gml
xboxlive_gamedisplayname_for_user(user_id);
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
for(var i = 0; i &amp;lt; xboxlive_get_user_count(); ++i;)
{
    user_id[i] = xboxlive_get_user(i);
    user_name[i] = xboxlive_gamedisplayname_for_user(user_id[i]);
}
```

The above code gets the user ID pointer for each available user account
and then stores the pointer along with the display name in two arrays.
