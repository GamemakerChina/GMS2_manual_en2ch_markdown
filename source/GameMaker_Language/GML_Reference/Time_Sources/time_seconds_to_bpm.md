# time_seconds_to_bpm

This function takes the length of a beat in seconds, and returns a
beats-per-minute value.

#### Syntax:

``` gml
time_seconds_to_bpm(seconds);
```

|          |                                                                      |                                                             |
|----------|----------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                 | Description                                                 |
| seconds  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The seconds-per-beat value to convert into beats-per-minute |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _period = time_source_get_period(time_source);
var _bpm = time_seconds_to_bpm(_period);

show_debug_message(_bpm);
```

This function gets the period of a Time Source , converts it to BPM and
prints that value to the output log. This code follows the example for [
time_bpm_to_seconds() ](time_bpm_to_seconds) .
