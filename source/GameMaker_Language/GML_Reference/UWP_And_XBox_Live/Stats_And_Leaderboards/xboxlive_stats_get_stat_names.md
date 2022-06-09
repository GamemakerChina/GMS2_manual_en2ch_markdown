# xboxlive_stats_get_stat_names

This function can be used to retrieve all the defined stats from the
stat manager for a given user. You supply the user ID as returned by
(for example) the function [ xboxlive_get_user()
](../Users_And_Accounts/xboxlive_get_user) , and the function will
return an array of strings containing the statistics for the user. If an
error occurs or the user has no stats the array will still be returned
but will have an element count of 0.

#### Syntax:

``` gml
xboxlive_stats_get_stat_names(user_id);
```

|          |                                                                                                                              |                                              |
|----------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                         | Description                                  |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID pointer to get the stat names of |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var _stat_str = xboxlive_stats_get_stat_names(user_id);
for (var i = 0; i &amp;lt; array_length(_stat_str); ++i;)
{
    xboxlive_stats_delete_stat(user_id, _stat_str[i]);
}
```

The above code retrieves all the defined stats for the user ID pointer
stored in the given variable, and then loops through the array and
deletes the specified stat from the stat manager.
