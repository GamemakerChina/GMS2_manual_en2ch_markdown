# time_source_get_time_remaining

This function returns the time remaining until the given Time Source
expires and executes its callback method. This time value will be
expressed in the [units](Time_Source_Units) set for the Time Source
(seconds or frames).

#### Syntax:

``` gml
time_source_get_time_remaining(id);
```

|          |                                                                                                      |                                          |
|----------|------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                 | Description                              |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to get information for   |

#### Returns:

``` gml
 Real
```
