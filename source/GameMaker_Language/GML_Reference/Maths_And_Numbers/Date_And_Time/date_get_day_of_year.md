# date_get_day_of_year

This function returns the day (from 1 to 366) within the year of the
given datetime.

#### Syntax:

``` gml
date_get_day_of_year( date );
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
mydayyear = date_get_day_of_year(date_current_datetime());
```

This would set mydayyear to the current day of the year.
