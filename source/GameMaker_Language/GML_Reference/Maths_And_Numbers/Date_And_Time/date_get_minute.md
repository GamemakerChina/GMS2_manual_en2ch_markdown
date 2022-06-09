# date_get_minute

This function returns the minute of the given datetime value.

#### Syntax:

``` gml
date_get_minute(date);
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
myminute = date_get_minute(date_current_datetime());
```

This would set "myminute" to the current minute.
