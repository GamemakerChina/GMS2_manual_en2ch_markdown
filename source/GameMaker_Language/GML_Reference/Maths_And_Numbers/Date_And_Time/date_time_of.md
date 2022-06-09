# date_time_of

Returns the time value of the given datetime. The time returned ignores
Daylight Saving Time (and so is Universal Time) and would normally be
used in conjunction with another date/time handling function.

#### Syntax:

``` gml
date_time_of(date);
```

|          |                                                                                                                         |                                        |
|----------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                    | Description                            |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to extract the time from. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
time = date_time_of(date_current_datetime());
```

This would return the current time only and store the value in the
variable "time".
