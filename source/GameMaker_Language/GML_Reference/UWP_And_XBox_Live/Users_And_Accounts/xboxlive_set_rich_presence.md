# xboxlive_set_rich_presence

This function will set the rich presence string for the given user. A
Rich Presence string shows a user's in-game activity after the name of
the game that the user is playing, separated by a hyphen. This string is
displayed under a player's Gamertag in the "Friends & Clubs" list as
well as in the player's Xbox Live user profile. When using this function
you need to supply the User ID pointer for the user, and then you can
flag the user as currently active in the game or not (using true / false
). If set to false , then the rich presence string will be appended with
"/afk" or something appropriate. The next argument is the rich presence
string ID to show, and then finally you can (optionally) supply a
service_config_id string. This argument is optional, and when not
supplied, it uses the SCID specified in the Xbox Game Options.

#### Syntax:

``` gml
xboxlive_set_rich_presence(user_id, is_user_active, rich_presence_string, [service_config_id]);
```

|                      |                                                                                                                              |                                                                                           |
|----------------------|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| Argument             | Type                                                                                                                         | Description                                                                               |
| user_id              |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The ID pointer of the user to check.                                                      |
| is_user_active       |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                    | Flag the user as active or not.                                                           |
| rich_presence_string |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The rich presence string ID to use (as defined in the Partner Center - max 50 characters) |
| service_config_id    |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     |  OPTIONAL This is the config_id string for the game.                                      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var pad_uid = xboxlive_user_for_pad(0);
xboxlive_set_rich_presence(pad_uid, true, "Playing_Challenge");
```

The above code gets the user ID pointer for the user assigned to the
gamepad \[0\] slot, and then sets the rich presence string for that
user.
