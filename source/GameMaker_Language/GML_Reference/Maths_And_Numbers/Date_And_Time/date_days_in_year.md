# date_days_in_year

With this function you can get the number of days that the given year
has, returning 365 for a normal year, and 366 for a leap year.

#### Syntax:

``` gml
date_days_in_year(date);
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
days = date_days_in_year(date_current_datetime());
```

This would set "days" to the number of days in the current year.
