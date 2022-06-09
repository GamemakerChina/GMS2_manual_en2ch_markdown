# date_get_week

This function returns the week of the given datetime value within the
year.

#### Syntax:

``` gml
date_get_week(date);
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
myweek = date_get_week(date_current_datetime());
```

This would set myweek to the current week.
