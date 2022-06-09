# xboxlive_achievements_set_progress

This function can be used to update the progress of an achievement. You
supply the user ID as returned, for example, by the function [
xboxlive_get_user() ](../Users_And_Accounts/xboxlive_get_user) , and
then the achievement string (this is the achievement id as assigned in
the XDP/Windows Dev Center when it was created). Finally you set the
progress value to to a value from 0 to 100. Note that the achievement
system will refuse updates that are lower than the current progress
value.

#### Syntax:

``` gml
xboxlive_achievements_set_progress(user_id, achievement, progress);
```

|             |                                                                                                                              |                                                    |
|-------------|------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument    | Type                                                                                                                         | Description                                        |
| user_id     |  [Xbox User ID](../../../../../GameMaker_Language/GML_Reference/UWP_And_XBox_Live/Users_And_Accounts/xboxlive_get_user)  | The user ID of the user to set the achievement for |
| achievement |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The achievement to set (a string)                  |
| progress    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                       | The progress value to set (from 0 to 100)          |

#### Returns:

``` gml
N/A
```

#### Extended Example:

The following is an extended example of how this function can be used.
To start with you'd call it in some event like **Room Start** or
**Create** :

``` gml
xboxlive_stats_get_social_leaderboard(user_id, "GlobalTime", 20, 1, false, false);
```

The above code would be called to get a list of all global leaderboard
positions for the game, and will generate a Social Asynchronous Event
call back which we would deal with in the following way:

``` gml
var _progress = (global.Level / global.LevelMax) * 100; xboxlive_achievements_set_progress(user_id, "Game_Completed", _progress);
```

The above code creates a percentage value based on some global variables
and then uses it to set the achievement progress for the
"Game_Completed" achievement.
