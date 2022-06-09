# time_source_create

This function creates a new Time Source . Read [Time
Sources](Time_Sources) for an overview. Creating a new Time Source
does not start it automatically; you must call [ time_source_start()
](time_source_start) to activate it. A new Time Source only runs
once, unless the repetitions argument is specified (read below). You
must destroy a Time Source using [ time_source_destroy()
](time_source_destroy) when you no longer need it.

## Arguments

Here is a breakdown of the function's arguments:

### [ Parent Time Source   Parent Time Source ](#)

This is the parent Time Source which controls the new Time Source . This
may be time_source_global , time_source_game or a custom Time Source
that already exists. See: [Built-In Time
Sources](Built_In_Time_Sources)

### [ Period   Period ](#)

This is a period of time that may be expressed in seconds or frames,
depending on the unit specified in the next argument. When using frames
as the unit, the period must be an integer. Non-integer values are
rounded down (floored), with the exception of values lower than 1, which
are rounded up to 1.

### [ Unit   Unit ](#)

This is the unit that the period is expressed in, and may be
time_source_units_seconds or time_source_units_frames . See: [Time
Source Units](Time_Source_Units) You can use a beats-per-minute
value by using [time_bpm_to_seconds()](time_bpm_to_seconds) .

### [ Callback & Args   Callback & Args ](#)

You must specify a "callback"
[method](../../GML_Overview/Method_Variables) that is called when
the Time Source expires. You can optionally specify an array containing
the arguments that should be passed into the method when it's called.
The array itself will not be passed into the method, rather each element
of the array will be passed as a separate argument. For example, if your
function expects the arguments (x, y, object) , then your args array may
look like this: \[30, 600, obj_player\] .

### [ Repetitions   Repetitions ](#)

You can optionally specify how many times your Time Source should
repeat. A value of 1 means it only runs once, which is the default
value. You can specify the total number of times it should repeat, or -1
to make it repeat indefinitely. For example, if you set this to 3, and
your Time Source period is "4 seconds", then the Time Source will be
active for a total of 12 seconds and will call the callback method every
4 seconds.

### [ Expiry Type   Expiry Type ](#)

This may be time_source_expire_nearest or time_source_expire_after .
See: [Time Source Expiry Types](Time_Source_Expiry_Types)

#### Syntax:

``` gml
time_source_create(parent, period, units, callback, [args, repetitions, expiry_type]);
```

|             |                                                                                                                         |                                                                                                       |
|-------------|-------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Argument    | Type                                                                                                                    | Description                                                                                           |
| parent      |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)                     | The parent Time Source that controls the new Time Source                                              |
| period      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The period that the Time Source runs for, in the given units                                          |
| units       |  [Time Source Unit Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_Units)           | The units that the given period is in                                                                 |
| callback    |  [Method](../../../../GameMaker_Language/GML_Overview/Method_Variables)                                             | The method to call when the Time Source expires                                                       |
| args        |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)                                                        |  OPTIONAL An array containing the arguments to pass into the method                                   |
| repetitions |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     |  OPTIONAL The number of times the Time Source should repeat, or -1 for indefinite repetition          |
| expiry_type |  [Time Source Expiry Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_Expiry_Types)  |  OPTIONAL Whether the Time Source expires on the frame nearest to its expiry, or on the next frame    |

#### Returns:

``` gml
 Time Source ID
```

#### Example 1:

``` gml
var _my_method = function()
{
    instance_destroy();
}

var _time_source = time_source_create(time_source_game, 300, time_source_units_frames, _my_method);

time_source_start(_time_source);
```

In this example, we want the instance to destroy itself 300 frames
later. The code first creates a method that simply calls [
instance_destroy() ](../Asset_Management/Instances/instance_destroy)
. It then creates a Time Source , inheriting from the Game Time Source .
It sets its period to **300 frames** . Finally, it starts the Time
Source .

#### Example 2:

``` gml
var _my_method = function()
{
    show_debug_message("A second has passed!");
}

global.time_per_second = time_source_create(time_source_game, 1, time_source_units_seconds, _my_method, [], -1, time_source_expire_after);

time_source_start(global.time_per_second);
```

In this example, we're creating a global Time Source that expires once
every second. This code would be placed at the root of a
[script](../../../The_Asset_Editors/Scripts) . The code first
creates a method that prints a message to the output log, saying **"A
second has passed!"** . It then creates a new Time Source , inheriting
from the Game Time Source . It sets its period to **1 second** . The
method is passed into the Time Source so it can be called each time it
expires. An empty array is given for the arguments. The repetition count
is set to -1, so the Time Source never stops and keeps repeating
forever. Its expiry type is set so the callback runs on the first frame
after its expiry. Finally, the Time Source is started.
