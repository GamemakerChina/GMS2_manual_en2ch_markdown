# current_month

This **read only** variable returns the current month as a numeric value
where 1 is January and 12 is December.

#### Syntax:

``` gml
current_month;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
draw_text((32, 32, "Today is " + string(current_day) + "/" + string (current_month) + "/" + string(current_year) +".");
```

The above code will draw the day, month and year.
