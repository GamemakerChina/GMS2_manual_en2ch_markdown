# xboxlive_stats_delete_stat

This function can be used to delete a stat from the stat manager for the
given user ID. You supply the user ID as returned by (for example) the
function [ xboxlive_get_user()
](../Users_And_Accounts/xboxlive_get_user) , then the stat string to
delete. This clears the stat value and removed it from the stat manager,
meaning it will no longer be returned by the functions [
xboxlive_stats_get_stat_names() ](xboxlive_stats_get_stat_names) or
[ xboxlive_stats_get_stat() ](xboxlive_stats_get_stat) . The
function will will return -1 if there was an error or the user ID is
invalid, or any other value if the function was successfully called

#### Syntax:

``` gml
xboxlive_stats_delete_stat(user_id, stat);
```

|          |                                                                                                                              |                                           |
|----------|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                         | Description                               |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID pointer to delete the stat of |
| stat     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The statistic to delete (a string)        |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
for(var i = 0; i &amp;lt; xboxlive_get_user_count(); i++;)
{
    user_id[i] = xboxlive_get_user(i);
    xboxlive_stats_delete_stat(user_id[i], "HighScore");
}
```

The above code loops through the connected users and deletes the
specified stat from the stat manager for each one.
