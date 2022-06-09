# date_create_datetime

This function will create a datetime value from the component given as
the arguments.

#### Syntax:

``` gml
date_create_datetime(year, month, day, hour, minute, second);
```

|          |                                                                         |                    |
|----------|-------------------------------------------------------------------------|--------------------|
| Argument | Type                                                                    | Description        |
| year     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The year to set.   |
| month    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The month to set.  |
| day      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The day to set.    |
| hour     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The hour to set.   |
| minute   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The minute to set. |
| second   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The second to set. |

#### Returns:

``` gml
 Datetime
```

#### Example:

``` gml
mydatetime = date_create_datetime(2011, 9, 15, 9, 43, 30);
```

This would set "mydatetime" to the given date and time and store the
returned value in the variable "mydatetime".
