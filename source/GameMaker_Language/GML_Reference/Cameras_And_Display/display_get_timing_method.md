# display_get_timing_method

This function can be used to retrieve the timing method to be used for
rendering your game. The method can be one of the constants listed
below. For more information on the different timing methods, please see
[ display_set_timing_method() ](display_set_timing_method) .

#### Syntax:

``` gml
display_get_timing_method();
```

#### Returns:

``` gml
 Display Timing Method Constant
```

|                                                                                                                                    |                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
|  [Display Timing Method Constant](../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/display_get_timing_method)  |                                                                              |
| Constant                                                                                                                           | Description                                                                  |
|  tm_sleep                                                                                                                          | The sleep margin value is the main timing method                             |
|  tm_countvsyncs                                                                                                                    | Vsync timing is the main timing method (default for all supported platforms) |

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
