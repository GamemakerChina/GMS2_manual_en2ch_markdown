# date_inc_hour

With this function you can increment a given datetime value by a
specific number of hours, and it will return the new datetime value.

#### Syntax:

``` gml
date_inc_hour(date, amount);
```

|          |                                                                                                                         |                                                  |
|----------|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                    | Description                                      |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to add to.                          |
| amount   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                  | The number of hours (must be an integer) to add. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
mynewdatetime = date_inc_hour(date_current_datetime(), 24);
```

This would set mynewdatetime to the current date but with 24 hours
added.
