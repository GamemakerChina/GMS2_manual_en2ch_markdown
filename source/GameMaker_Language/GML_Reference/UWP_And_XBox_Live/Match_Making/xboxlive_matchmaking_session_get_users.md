# xboxlive_matchmaking_session_get_users

This function will create and populate a DS map with the details of the
users in the specified session, or -1 if there is an error. You can get
the session ID pointer from the [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
DS map that is returned in the [Asynchronous Social
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/Social)
when you created or found a session (see [ xboxlive_matchmaking_create()
](xboxlive_matchmaking_create) for more details). The returned DS
map will have the following key/value pairs:

-   " **num_results** " - contains the number of users in the session
-   " **userId\< *index* \>** " - contains the ID of the user (\<
    *index* \> is a value from 0 to "num_results" - 1)
-   " **userIsOwner\< *index* \>** " - contains 1 if the user is the
    host, otherwise 0 (\< *index* \> is a value from 0 to
    "num_results" - 1)

#### Syntax:

``` gml
xboxlive_matchmaking_session_get_users(session_id);
```

|            |                                                                         |                               |
|------------|-------------------------------------------------------------------------|-------------------------------|
| Argument   | Type                                                                    | Description                   |
| session_id |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The session ID pointer to use |

#### Returns:

``` gml
 Async Request ID
```

#### Example:

``` gml
var session_map = xboxlive_matchmaking_session_get_users(global.SessionID);
if (session_map != -1)
{
    for (var i = 0; i &amp;lt; session_map[? "num_results"]; i++)
    {
        if (session_map[? "userIsOwner" + string(i)] == 1)
        {
            global.OwnerID = session_map[? "userId" + string(i)];
        }
    }
}
```

The above will retrieve the user data for all users participating in the
matchmaking session and set a global variable to the ID of the session
owner.
