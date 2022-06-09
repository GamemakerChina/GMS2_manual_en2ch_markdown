# time_source_reset

This function resets the given Time Source , resetting its timer and
repetition information. After calling this function, you will need to
[start](time_source_start) the Time Source again for it to count
down.

#### Syntax:

``` gml
time_source_reset(id);
```

|          |                                                                                                      |                            |
|----------|------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                 | Description                |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to reset   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
// Room Start event
time_source_reset(global.spawn_time_source);
time_source_start(global.spawn_time_source);
```

This code will reset the given Time Source whenever a new room starts,
and then start the Time Source again.
