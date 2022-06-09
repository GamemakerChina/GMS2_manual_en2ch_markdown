# current_hour

This **read only** variable will return the hour that corresponds to the
current moment based on the default time zone for the system (ie: local
time). You can change the base time zone to use with the function [
date_set_timezone() ](date_set_timezone) .

#### Syntax:

``` gml
current_hour;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
draw_text(32, 32, "The time is " + string(current_hour) + ":" + string(current_minute) + "." + string(current_second));
```

The above code would draw the current international time on the screen.
