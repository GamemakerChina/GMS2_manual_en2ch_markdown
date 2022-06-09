# date_get_hour

This function returns the hour of the given datetime value.

#### Syntax:

``` gml
date_get_hour(date);
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
myhour = date_get_hour(date_current_datetime());
```

This would set "myhour" to the current hour.
