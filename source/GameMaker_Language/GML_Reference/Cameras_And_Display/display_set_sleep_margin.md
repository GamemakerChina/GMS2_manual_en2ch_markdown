# display_set_sleep_margin

This function can be used to set the sleep margin value used for the
render timing of your game, and requires a millisecond value. The
default values are as follows:

|                 |              |
|-----------------|--------------|
| Platform        | Milliseconds |
| Windows         | 10           |
| macOS           | 10           |
| Ubuntu          | 10           |
| HTML5           | 10           |
| Android         | 4            |
| iOS             | 4            |
| Windows UWP     | 10           |
| Xbox            | 10           |
| PS4             | 10           |
| Nintendo Switch | 10           |

Note that even if the timing method is set to use vsync timing, the
sleep margin will have some effect over the rendering of the game, and
so you should take care when setting this value. For more information on
display timing, please see [ display_set_timing_method()
](display_set_timing_method) . **NOTE** : In addition to the Sleep
Margin, you can further control your performance and power consumption
on Windows by adjusting the [thread scheduler's
resolution](../OS_And_Compiler/scheduler_resolution_set) at runtime.

#### Syntax:

``` gml
display_set_sleep_margin(milliseconds);
```

|              |                                                                      |                                                 |
|--------------|----------------------------------------------------------------------|-------------------------------------------------|
| Argument     | Type                                                                 | Description                                     |
| milliseconds |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The number of milliseconds for the sleep margin |

#### Returns:

``` gml
N/A
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
