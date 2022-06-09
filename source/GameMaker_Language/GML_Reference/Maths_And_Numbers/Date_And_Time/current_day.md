# current_day

This **read only** variable will return the day as a value from 1 to 31,
depending on the month.

#### Syntax:

``` gml
current_day;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
draw_text(32, 32, "Today is " + string(current_day) + "/" + string (current_month) + "/" + string(current_year) +".");
```

The above code will draw the day, month and year.
