# time_source_get_reps_remaining

This function returns the number of repetitions the given Time Source
has left until it completely stops. The function will return undefined
if the given Time Source runs indefinitely, or if it's a [built-in Time
Source ](Built_In_Time_Sources) .

#### Syntax:

``` gml
time_source_get_reps_remaining(id);
```

|          |                                                                                                      |                                          |
|----------|------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                 | Description                              |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to get information for   |

#### Returns:

``` gml
 Real
```
