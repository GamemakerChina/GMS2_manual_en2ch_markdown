# time_source_stop

This function stops the given Time Source and resets its timer.

#### Syntax:

``` gml
time_source_stop(id);
```

|          |                                                                                                      |                           |
|----------|------------------------------------------------------------------------------------------------------|---------------------------|
| Argument | Type                                                                                                 | Description               |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to stop   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (time_source_get_state(time_source) != time_source_state_stopped)
{
    time_source_stop(time_source);
}
```

The code above will stop a Time Source when it's not already stopped.
