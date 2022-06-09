# date_days_in_month

With this function you can get the number of days that the given month
has, either 28, 29, 30 or 31.

#### Syntax:

``` gml
date_days_in_month(date);
```

|          |                                                                                                                         |                  |
|----------|-------------------------------------------------------------------------------------------------------------------------|------------------|
| Argument | Type                                                                                                                    | Description      |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The date to use. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
days = date_days_in_month(date_current_datetime());
```

This would set "days" to the number of days in the current month.
