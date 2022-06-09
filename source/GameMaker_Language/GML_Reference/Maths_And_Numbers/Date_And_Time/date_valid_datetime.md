# date_valid_datetime

With this function you can check a datetime value to see if it is valid
(returns true ) or not (returns false ). Note that this function will
only consider a valid datetime as being *after* 1/1/1970 and anything
before that will return false , so the earliest you can check would be:

``` gml
date_valid_datetime(1970, 01, 01, 0, 0, 0);
```

#### Syntax:

``` gml
date_valid_datetime(year, month, day, hour, minute, second);
```

|          |                                                                         |                      |
|----------|-------------------------------------------------------------------------|----------------------|
| Argument | Type                                                                    | Description          |
| year     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The year to check.   |
| month    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The month to check.  |
| day      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The day to check.    |
| hour     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The hour to check.   |
| minute   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The minute to check. |
| second   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The second to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if date_valid_datetime(2011, 9, 15, 10, 3, 30)
{
    mydatetime = date_create_datetime(2011, 9, 15, 10, 3, 30);
}
```

This will set "mydatetime" to 15th September 2011, 10:03.30, if it is a
valid value (which it is).
