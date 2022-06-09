# date_set_timezone

Sets the base time zone to use for all the rest of the date and time
functions. This time zone can either be *local* (as set by the system)
or *UTC* , and you would use one of the following constants to define
which is being used (by default this is local time):

|                  |                                              |
|------------------|----------------------------------------------|
| Constant         | Description                                  |
|  timezone_local  | use the local time zone as set by the system |
|  timezone_utc    | use Coordinated Universal Time               |

#### Syntax:

``` gml
date_set_timezone(timezone);
```

|          |                                                                                                                               |                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                          | Description                             |
| timezone |  [Time Zone Constant](../../../../../GameMaker_Language/GML_Reference/Maths_And_Numbers/Date_And_Time/date_get_timezone)  | The time zone to use for the base time. |

#### Returns:

``` gml
N/A
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
