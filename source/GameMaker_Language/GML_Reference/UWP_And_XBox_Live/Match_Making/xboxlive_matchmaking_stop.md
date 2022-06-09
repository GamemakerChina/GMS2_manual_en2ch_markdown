# xboxlive_matchmaking_stop

This function can be used to end a matchmaking session for the given
user.

#### Syntax:

``` gml
xboxlive_matchmaking_stop(user_id);
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
if !xboxlive_user_is_signed_in(user_id[0])
{
    xboxlive_matchmaking_stop(user_id[0]);
}
```

The above code will end the matchmaking session for the given user.
