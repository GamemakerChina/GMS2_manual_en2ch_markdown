# time_source_pause

This function pauses the given Time Source . To resume it, call [
time_source_start() ](time_source_start) .

#### Syntax:

``` gml
time_source_pause(id);
```

|          |                                                                                                      |                            |
|----------|------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                 | Description                |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to pause   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (keyboard_check_pressed(vk_space))
{
    var _state = time_source_get_state(time_source);

    if (_state == time_source_state_active)
    {
        time_source_pause(time_source);
    }
    else if (_state == time_source_state_paused)
    {
        time_source_start(time_source);
    }
}
```

When the Space key is pressed, this code will get a Time Source 's
state. When the state is active, it will pause the Time Source , and
when it's paused, it will resume it.
