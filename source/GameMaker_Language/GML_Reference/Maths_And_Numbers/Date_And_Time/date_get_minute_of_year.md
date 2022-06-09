# date_get_minute_of_year

This function returns the minute of the given datetime value within the
year (from the total number of minutes for the year, taking into account
leap years).

#### Syntax:

``` gml
date_get_minute_of_year(date);
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
myminuteyear = date_get_minute_of_year(date_current_datetime());
```

This would set myminuteyear to the current minute of the year.
