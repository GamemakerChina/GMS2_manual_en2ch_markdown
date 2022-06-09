# date_get_weekday

This function returns the week day value of the given datetime. This
will be a value from 0 to 6.

#### Syntax:

``` gml
date_get_weekday(date);
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
myweekday = date_get_weekday(date_current_datetime());
```

This would set "myweekday" to the current weekday.
