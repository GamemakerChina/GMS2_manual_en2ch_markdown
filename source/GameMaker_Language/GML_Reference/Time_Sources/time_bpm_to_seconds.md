# time_bpm_to_seconds

This function takes a beats-per-minute value, and returns the length of
each beat in seconds. This can be used when [creating a Time
Source](time_source_create) to use a BPM value for the Time Source .
It's important that such a Time Source uses **seconds** as its
[unit](Time_Source_Units) .

#### Syntax:

``` gml
time_bpm_to_seconds(bpm);
```

|          |                                                                      |                                                             |
|----------|----------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                 | Description                                                 |
| bpm      |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The beats-per-minute value to convert into seconds-per-beat |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _bpm = 90;
var _seconds = time_bpm_to_seconds(_bpm);

time_source = time_source_create(time_source_game, _seconds, time_source_units_seconds, function()
{
    show_debug_message("BEAT!");
}, [], -1);
```

This code converts a value of 90 BPM into seconds, and uses that to
create a Time Source that runs indefinitely. On each beat, it prints the
message "BEAT!" to the output log.
