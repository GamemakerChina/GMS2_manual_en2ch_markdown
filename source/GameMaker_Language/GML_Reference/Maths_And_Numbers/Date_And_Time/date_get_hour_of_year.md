# date_get_hour_of_year

This function returns the hour of the given datetime value within the
year (from the total number of hours for the year, taking into account
leap years).

#### Syntax:

``` gml
date_get_hour_of_year(date);
```

|          |                                                                                                                         |                        |
|----------|-------------------------------------------------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                                                                    | Description            |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
myhouryear = date_get_hour_of_year(date_current_datetime());
```

This would set "myhouryear" to the current hour of the year.
