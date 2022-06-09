# date_get_year

This function returns the year of the given datetime.

#### Syntax:

``` gml
date_get_year(date);
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
myyear = date_get_year(date_current_datetime());
```

This would set "myyear" to the current year.
