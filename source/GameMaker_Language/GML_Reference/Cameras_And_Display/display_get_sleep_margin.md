# display_get_sleep_margin

This function can be used to get the current sleep margin value used for
the render timing of your game, and will return a millisecond value. For
more information on display timing, please see [
display_set_timing_method() ](display_set_timing_method) .

#### Syntax:

``` gml
display_get_sleep_margin();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if display_get_timing_method() != tm_sleep
{
    display_set_timing_method(tm_sleep);
    if display_get_sleep_margin() != 20
    {
        display_set_sleep_margin(20);
    }
}
```

The above code will check the timing method and then if it's not set to
tm_sleep it will be set to that and the sleep margin set to 20.
