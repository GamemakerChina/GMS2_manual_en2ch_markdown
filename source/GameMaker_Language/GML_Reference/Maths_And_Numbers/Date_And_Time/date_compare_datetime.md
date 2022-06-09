# date_compare_datetime

With this function you can check two dates and times to see which one is
the earlier or later than the other. The function returns -1 if
**date1** is earlier, 1 if **date1** is later and 0 if they are the
same, although since this takes time into account as well, a 0 for
matching is very rare (it literally has to be the same second of the
same day of the same month of the same year to return a 0).

#### Syntax:

``` gml
date_compare_datetime(date1, date2);
```

|          |                                                                                                                         |                                |
|----------|-------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                                    | Description                    |
| date1    |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The first datetime.            |
| date2    |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to compare it to. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
d = date_compare_datetime(date_create_datetime(2011, 9, 15, 11, 4, 0), date_current_datetime());
```

This would set d to the corresponding value depending on which of the
datetimes was the earliest, likely -1 since the current date would be
further ahead than 15th September 2011.
