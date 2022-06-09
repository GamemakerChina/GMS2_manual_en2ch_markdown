# current_second

This **read only** variable will return the seconds that correspond to
the current moment.

#### Syntax:

``` gml
current_second;
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
