# xboxlive_matchmaking_session_leave

This function causes the user who created or found the specified session
to leave it. You can get the session ID pointer from the [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
DS map that is returned in the [Asynchronous Social
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/Social)
when you created or found a session (see [ xboxlive_matchmaking_create()
](xboxlive_matchmaking_create) for more details).

#### Syntax:

``` gml
xboxlive_matchmaking_session_leave(session_id);
```

|            |                                                                         |                                                 |
|------------|-------------------------------------------------------------------------|-------------------------------------------------|
| Argument   | Type                                                                    | Description                                     |
| session_id |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The Session ID pointer of the session to leave. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if gamepad_button_check_pressed(0, gp_start)
{
    xboxlive_matchmaking_session_leave(global.SessionID);
}
```

The above code checks for a gamepad button press and if one is detected
then the user will logged out of the given matchmaking session.
