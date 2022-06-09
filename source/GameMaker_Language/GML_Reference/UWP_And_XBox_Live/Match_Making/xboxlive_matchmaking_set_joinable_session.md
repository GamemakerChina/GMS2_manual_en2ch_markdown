# xboxlive_matchmaking_set_joinable_session

This function sets a (previously created) session to be available for
other users to join through the system UI. A user only has one joinable
session at once, and when they leave the session (or the session ends)
this will be cleared, however you can clear it manually by passing -1 in
for the session argument.

#### Syntax:

``` gml
xboxlive_matchmaking_set_joinable_session(local_user, session_that_is_joinable);
```

|                          |                                                                                                                              |                                         |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument                 | Type                                                                                                                         | Description                             |
| local_user               |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The local user ID pointer.              |
| session_that_is_joinable |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The session ID to make joinable, or -1. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (global.session_ID != -1)
{
    xboxlive_matchmaking_set_joinable_session(xboxlive_user_for_pad(0), global.session_ID);
}
```

The above code checks for a valid session ID value, and if one is
detected it sets the session to be joinable.
