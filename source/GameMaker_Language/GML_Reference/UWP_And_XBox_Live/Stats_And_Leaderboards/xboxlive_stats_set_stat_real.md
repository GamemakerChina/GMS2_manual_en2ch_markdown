# xboxlive_stats_set_stat_real

This function can be used to set the value of a stat for the given user
ID. You supply the user ID as returned by (for example) the function [
xboxlive_get_user() ](../Users_And_Accounts/xboxlive_get_user) ,
then the stat string to set ( **if the stat string does not already
exist then a new stat will be created and set to the given value** ) and
a value (a real) to set the stat to. Note that the stat name must be
alphanumeric only, with no symbols or spaces. When setting the stat
value, any previous value will be overridden, therefore it is up to you
to determine if the stat value should be updated or not (ie. check that
the high score is actually the highest) by comparing to the current stat
value with the new one before setting it. The function will will return
-1 if there was an error or the user ID is invalid, or any other value
if the function was successfully called.

#### Syntax:

``` gml
xboxlive_stats_set_stat_real(user_id, stat, value);
```

|          |                                                                                                                              |                                         |
|----------|------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                         | Description                             |
| user_id  |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID pointer to set the stat for |
| stat     |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The statistic to set (a string)         |
| value    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The value to set the stat to (a real)   |

#### Returns:

``` gml
 Real
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
