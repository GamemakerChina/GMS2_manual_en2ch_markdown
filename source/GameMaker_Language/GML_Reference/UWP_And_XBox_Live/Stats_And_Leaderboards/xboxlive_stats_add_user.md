# xboxlive_stats_add_user

This function can be used to add a given user ID pointer to the
statistics manager. This must be done before using any of the other
stats functions to automatically sync the game with the XBox Live server
and retrieve the latest values. You supply the user ID as returned by
(for example) the function [ xboxlive_get_user()
](../Users_And_Accounts/xboxlive_get_user) , and the function will
will return -1 if there was an error or if the user ID is invalid, or
any other value if the function was successfully called. The function
will generate a callback which will trigger a [System Asynchronous
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/System)
. This event will have the special DS map [ async_load
](../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
which should then be parsed for the following keys:

-   " **id** " - Will hold the constant achievement_stat_event
-   " **eventname** " - Will hold the string " *LocalUserAdded* "
-   " **userid** " - The user ID associated with the request
-   " **error** " - 0 if successful, some other value if there has been
    an error
-   " **errormessage** " - A string with an error message, if any is
    available

#### Syntax:

``` gml
xboxlive_stats_add_user(user_id);
```

|          |                                                                                                                              |                                |
|----------|------------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                                         | Description                    |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID (a pointer) to add |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; xboxlive_get_user_count(); ++i;)
{
    user_id[i] = xboxlive_get_user(i);
    xboxlive_stats_add_user(user_id[i]);
}
```

The above code will get the number of user accounts available then loop
through them and assign the account ID to an array, as well as register
the user with the stats manager.
