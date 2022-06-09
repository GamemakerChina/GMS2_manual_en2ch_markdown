# date_is_today

This function will return true if the given datetime value is the day it
is being checked on (ie: today), or false otherwise. This can be a handy
function for things like Easter Eggs in your games, or for unlocking
seasonal content. Note that this function will be affected by the time
zone set (default is local time) which you can change using the [
date_set_timezone() ](date_set_timezone) function.

#### Syntax:

``` gml
date_is_today(date);
```

|          |                                                                                                                         |                      |
|----------|-------------------------------------------------------------------------------------------------------------------------|----------------------|
| Argument | Type                                                                                                                    | Description          |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to use. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if date_is_today(global.Halloween)
{
    global.Max_Levels = 200;
}
```

The above code will check the datetime stored in the global variable
"Halloween" to see if it is today, and if it is it sets another global
variable to a new value.
