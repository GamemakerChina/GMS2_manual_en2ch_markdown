# current_weekday

This **read only** variable will return the weekday as a value, where
Sunday is 0 and Saturday is 6.

#### Syntax:

``` gml
current_weekday;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var day;
switch(current_weekday)
{
    case 0: day = "Sunday"; break;
    case 1: day = "Monday"; break;
    case 2: day = "Tuesday"; break;
    case 3: day = "Wednesday"; break;
    case 4: day = "Thursday"; break;
    case 5: day = "Friday"; break;
    case 6: day = "Saturday"; break;
}
draw_text(32, 32, "Today is " + day +".");
```

The above code uses the current_weekday value to set a variable with the
correct day in text, then draws that for the user to see.
