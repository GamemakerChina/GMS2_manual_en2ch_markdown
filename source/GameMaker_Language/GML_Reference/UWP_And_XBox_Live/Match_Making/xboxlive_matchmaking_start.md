# xboxlive_matchmaking_start

This function must be called before you can start any multi-player
session for the user. It takes the User ID pointer, which you can
retrieve for a particular game pad by calling the [
xboxlive_user_for_pad()
](../Users_And_Accounts/xboxlive_user_for_pad) function, and will
initialise the multi-player API.

#### Syntax:

``` gml
xboxlive_matchmaking_start(user_id);
```

|          |                                                                                                                              |                            |
|----------|------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                                         | Description                |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID pointer to use |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
global.UserID = xboxlive_user_for_pad(global.PadIndex); xboxlive_matchmaking_start(global.UserID);
```

The above code gets the user ID for the given pad index and then
initialises multiplayer capabilities.
