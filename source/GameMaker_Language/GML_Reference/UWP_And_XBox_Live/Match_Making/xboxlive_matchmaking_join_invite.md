# xboxlive_matchmaking_join_invite

This function can be called to process a join invitation once you have
successfully called [ xboxlive_matchmaking_start()
](xboxlive_matchmaking_start) . You supply the local UserID and the
the invitation values (ID and host ID) which were returned when the
invitation was received, along with the name of the Session Template
that you created (a string). It will then join the user to the session
they've been invited to, and you will receive Social Asynchronous Events
as if you had called [ xboxlive_matchmaking_find()
](xboxlive_matchmaking_find) .

#### Syntax:

``` gml
xboxlive_matchmaking_join_invite(user_who_received_invite, invitation_id, invitation_host, sda_template_name);
```

|                          |                                                                                                                              |                            |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Argument                 | Type                                                                                                                         | Description                |
| user_who_received_invite |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The local user ID pointer. |
| invitation_id            |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The invitation ID.         |
| invitation_host          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The invitation host ID.    |
| sda_template_name        |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The session template name. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var userID = xboxlive_user_for_pad(global.PadIndex); xboxlive_matchmaking_join_invite(userID, global.InviteID, global.InviteHost, global.SessionTemplate);
```

The above gets the user ID for the given gamepad and then attaempt to
join the session that they have been invited to.
