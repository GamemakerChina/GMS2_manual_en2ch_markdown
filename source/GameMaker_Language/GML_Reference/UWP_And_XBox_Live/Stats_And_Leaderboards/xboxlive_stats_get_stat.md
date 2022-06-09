# xboxlive_stats_get_stat

This function can be used to retrieve a single stat value from the stat
manager for a given user. You supply the user ID as returned by (for
example) the function [ xboxlive_get_user()
](../Users_And_Accounts/xboxlive_get_user) , and then the stat
string as defined when you created it using the one of the
xboxlive_stats_set_stat\_\* functions. The return value can be either a
string or a real (depending on the stat being checked) or the GML
constant undefined if the stat does not exist or there has been an
error.

#### Syntax:

``` gml
xboxlive_stats_get_stat(user_id, stat);
```

|          |                                                                                                                              |                                              |
|----------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                         | Description                                  |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID pointer to get the stat names of |
| stat     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The statistic to set (a string)              |

#### Returns:

``` gml
 Real

,

 String

or

 undefined
```

#### Example:

``` gml
if (game_over == true)
{
    if (xboxlive_stats_get_stat(p_user_id, "PercentDone") &amp;lt; 100)
    {
        var _val = (global.LevelsFinished / global.LevelsTotal) * 100;
        xboxlive_stats_set_stat_real(p_user_id, "PercentDone", _val);
    }
}
```

The above code checks a variable and if it's true , then it will check
the value of the "PercentDone" stat. If this value is less than 100, a
value is then generated and the stat set to that value.
