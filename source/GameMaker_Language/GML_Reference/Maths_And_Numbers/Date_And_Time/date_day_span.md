# date_day_span

With this function you can get the number of days between two dates.
This value is always positive, and incomplete days will be returned as a
fraction.

#### Syntax:

``` gml
date_day_span(date1, date2);
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
diff = date_day_span(date_create_datetime(2011, 9, 15, 11, 4, 0), date_current_datetime());
```

This would set diff to the number of days between 15th September 2011,
11:04.0 and the current date and time.
