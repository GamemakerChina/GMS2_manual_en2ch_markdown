# date_get_day

This function returns the day (from 1 to 31) of the given datetime.

#### Syntax:

``` gml
date_get_day(date);
```

|          |                                                                                                                         |                    |
|----------|-------------------------------------------------------------------------------------------------------------------------|--------------------|
| Argument | Type                                                                                                                    | Description        |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The date to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
myday = date_get_day( date_current_datetime() );
```

This would set "myday" to the current day.
