# date_compare_date

With this function you can check two dates to see which one is the
earlier or later than the other. The function returns -1 if **date1** is
earlier, 0 if both dates are the same, and 1 if **date1** is later.

#### Syntax:

``` gml
date_compare_date( date1, date2 );
```

|          |                                                                                                                         |                            |
|----------|-------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                                    | Description                |
| date1    |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The first date.            |
| date2    |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The date to compare it to. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
d = date_compare_date(date_create_datetime(2011, 9, 15, 11, 4, 0), date_current_datetime());
```

This would set "d" to the corresponding value depending on which of the
dates was the earliest, likely 1 since the current date would be further
ahead than 15th September 2011.
