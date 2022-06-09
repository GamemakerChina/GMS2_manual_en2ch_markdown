# time_source_get_reps_completed

This function returns the number of repetitions the given Time Source
has completed since its last [reset](time_source_reset) . That would
be the number of times it has expired and executed its callback method.

#### Syntax:

``` gml
time_source_get_reps_completed(id);
```

|          |                                                                                                      |                                          |
|----------|------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                 | Description                              |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to get information for   |

#### Returns:

``` gml
 Real
```
