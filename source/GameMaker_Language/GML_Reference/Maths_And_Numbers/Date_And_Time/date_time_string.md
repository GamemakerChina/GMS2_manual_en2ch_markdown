# date_time_string

With this function you can create a string containing the given time,
formatted for the system or device that is running the game when the
function is called.

#### Syntax:

``` gml
date_time_string( date );
```

|          |                                                                                                                         |                      |
|----------|-------------------------------------------------------------------------------------------------------------------------|----------------------|
| Argument | Type                                                                                                                    | Description          |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to use. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str = date_time_string(date_current_datetime());
```

This would set the given variable to something like "11:36.00" depending
on the system settings for date/time displaying and the current date and
time.
