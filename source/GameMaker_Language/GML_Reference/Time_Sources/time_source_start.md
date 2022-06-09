# time_source_start

This function starts the given Time Source , changing its
[state](Time_Source_States) to time_source_state_active . The
specified Time Source may be a new Time Source that was never
started, was paused, stopped or expired with no repetitions. This
function will "soft-reset" the given Time Source , resetting its [expiry
time](time_source_get_time_remaining) and [reps
remaining](time_source_get_reps_remaining) to the values that were
configured for it.

#### Syntax:

``` gml
time_source_start(id);
```

|          |                                                                                                      |                            |
|----------|------------------------------------------------------------------------------------------------------|----------------------------|
| Argument | Type                                                                                                 | Description                |
| id       |  [Time Source ID](../../../../GameMaker_Language/GML_Reference/Time_Sources/time_source_create)  | The Time Source to start   |

#### Returns:

``` gml
N/A
```

#### Example:

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
