# date_date_string

With this function you can create a string containing the given date,
formatted as day/month/year.

#### Syntax:

``` gml
date_date_string(date);
```

|          |                                                                                                                         |                  |
|----------|-------------------------------------------------------------------------------------------------------------------------|------------------|
| Argument | Type                                                                                                                    | Description      |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The date to use. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
str = date_date_string(date_current_datetime()); draw_text(32, 32, str);
```

This would set "str" to hold a formatted string of the current date and
time as shown by the system.
