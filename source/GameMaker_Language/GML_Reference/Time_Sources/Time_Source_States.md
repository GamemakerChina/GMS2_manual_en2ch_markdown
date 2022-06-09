# Time Source States

|                                                                                                                  |                                                                                  |       |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-------|
|  [Time Source State Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_States)  |                                                                                  |       |
| Constant                                                                                                         | Description                                                                      | Value |
|  time_source_state_initial                                                                                       | The Time Source has not been started yet                                         | 0     |
|  time_source_state_active                                                                                        | The Time Source has been [started](time_source_start) and is counting down   | 1     |
|  time_source_state_paused                                                                                        | The Time Source is [paused](time_source_pause)                               | 2     |
|  time_source_state_stopped                                                                                       | The Time Source was [stopped](time_source_stop) or it completely expired     | 3     |

A Time Source can have a state, which can be any one of the constants
above. The default state for a newly-created Time Source is
time_source_state_initial . The state can be changed using [
time_source_start() ](time_source_start) , [ time_source_stop()
](time_source_stop) , and [ time_source_pause()
](time_source_pause) . The state of a Time Source is returned using
[ time_source_get_state() ](time_source_get_state) .
