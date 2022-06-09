# date_date_of

Returns the date value of the given datetime.

#### Syntax:

``` gml
date_date_of(date);
```

|          |                                                                                                                         |                                        |
|----------|-------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                    | Description                            |
| date     |  [Datetime](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_current_datetime)  | The datetime to extract the date from. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
today = date_date_of(date_current_datetime());
```

This would return the current date only and store the value in the
variable "today".
