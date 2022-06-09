# date_get_timezone

This function gets the base time zone being used for all the rest of the
date and time functions. This time zone can either be *local* (as set by
the system) or *UTC* , and the function will return one of the following
constants:

|                                                                                                                               |                                              |
|-------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
|  [Time Zone Constant](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_get_timezone)  |                                              |
| Constant                                                                                                                      | Description                                  |
|  timezone_local                                                                                                               | use the local time zone as set by the system |
|  timezone_utc                                                                                                                 | use Coordinated Universal Time               |

#### Syntax:

``` gml
date_get_timezone();
```

#### Returns:

``` gml
 Time Zone Constant
```

#### Example:

``` gml
if (date_get_timezone() != timezone_utc)
{
    date_set_timezone(timezone_utc);
}
```

This code checks the base time zone setting for the game and if it is
not UTC it then changes it.
