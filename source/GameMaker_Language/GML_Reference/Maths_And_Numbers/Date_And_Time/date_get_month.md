# date_get_month

This function returns the month of the given datetime value.

#### Syntax:

``` gml
date_get_month(date);
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
mymonth = date_get_month(date_current_datetime());
```

This would set mymonth to the current month.
