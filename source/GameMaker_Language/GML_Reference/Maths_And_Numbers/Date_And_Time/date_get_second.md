# date_get_second

This function returns the second of the given datetime value.

#### Syntax:

``` gml
date_get_second(date);
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
mysecond = date_get_second(date_current_datetime());
```

This would set mysecond to the current second.
