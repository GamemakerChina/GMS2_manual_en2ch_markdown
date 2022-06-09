# xboxlive_stats_setup

This function needs to be called before you can use any of the other
Xbox Live stat functions, and simply initialises the required libraries
on the system. The "user_id" argument is the raw user ID as returned by
the function [ xboxlive_get_user()
](../Users_And_Accounts/xboxlive_get_user) , while the
"service_config" and "title_id" is the unique ID for your game on the
Xbox Live Dev Center. This function is only for use with Event-Based
(2013) stats.

#### Syntax:

``` gml
xboxlive_stats_setup(user_id, service_config_id, title_id);
```

|                   |                                                                                                                              |                                                     |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument          | Type                                                                                                                         | Description                                         |
| user_id           |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The ID pointer of the user to check.                |
| service_config_id |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | This is the config_id string for the game.          |
| title_id          |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The unique ID for your game on the Xbox Dev Center. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var user = xboxlive_get_user(0);
xboxlive_stats_setup(user, "4d61a1aa-61ac-4541-badd-31f91244fea6", $1244FEA6);
```

The above code initialises the stats system for the given user ID.
