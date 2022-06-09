# date_current_datetime

Returns the date-time value of the current moment. The time returned is
based on the default time zone for the system (ie: local time). You can
change the base time zone to use with the function [ date_set_timezone()
](date_set_timezone) .

#### Syntax:

``` gml
date_current_datetime();
```

#### Returns:

``` gml
 Datetime
```

#### Example:

``` gml
myhour = date_get_hour(date_current_datetime());
myday = date_get_day(date_current_datetime());
```

This would set local variable myhour to the hour of the current time,
and myday to the day of the current date.
