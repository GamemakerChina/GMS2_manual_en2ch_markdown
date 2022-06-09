# GM_build_date

This constant holds the date and time on which the executable being run
was built by GameMaker . The value can be parsed using the [Date and
Time](../Maths_And_Numbers/Date_And_Time/Date_And_Time) functions
and is taken from the system UTC value at compile time.

#### Syntax:

``` gml
GM_build_date;
```

#### Returns:

``` gml
 Datetime
```

#### Example:

``` gml
draw_text(32, 32, date_time_string(GM_build_date));
draw_text(32, 64, "v" + GM_version);
```

The above code will draw the version number for the game and the date
and time it was compiled on.
