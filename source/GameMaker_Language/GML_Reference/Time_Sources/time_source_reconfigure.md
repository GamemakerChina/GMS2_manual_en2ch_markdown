# time_source_reconfigure

This function is used to modify the core properties of a Time Source ,
without having to create an entirely new one. You specify an existing
Time Source , and then set the properties that are also set in [
time_source_create() ](time_source_create) , except the parent. Read
that page for detailed information on these properties. The specified
Time Source will be reset and deactivated, and will need to be
[started](time_source_start) again.

#### Syntax:

``` gml
time_source_reconfigure(id, period, units, callback, [args, repetitions, expiry_type]);
```

|             |                                                                                                                         |                                                                                                       |
|-------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Argument    | Type                                                                                                                    | Description                                                                                           |
| id          |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)                     | The Time Source to reconfigure                                                                        |
| period      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The period that the Time Source runs for, in the given units                                          |
| units       |  [Time Source Unit Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_Units)           | The units that the given period is in                                                                 |
| callback    |  [Method](../../../../GameMaker_Language/GML_Overview/Method_Variables)                                             | The method to call when the Time Source expires                                                       |
| args        |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)                                                        |  OPTIONAL An array containing the arguments to pass into the method                                   |
| repetitions |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     |  OPTIONAL The number of times the Time Source should repeat, or -1 for indefinite repetition          |
| expiry_type |  [Time Source Expiry Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_Expiry_Types)  |  OPTIONAL Whether the Time Source expires on the frame nearest to its expiry, or on the next frame    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
function change_spawn_delay(new_delay)
{
    time_source_reconfigure(obj_game.spawn_time_source, new_delay, time_source_units_frames, obj_game.spawn_method, [], -1);
    time_source_start(obj_game.spawn_time_source);
}
```

This creates a new function that changes the spawn delay used for
in-game enemies. Assuming the game uses a Time Source called
obj_game.spawn_time_source to spawn enemies, that Time Source will need
to be updated once the spawn delay changes. This function does exactly
that, reconfiguring the Time Source with the new delay and then
[starting it](time_source_start) again.
