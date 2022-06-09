# Time Source Units

|                                                                                                                |                                                              |       |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|-------|
|  [Time Source Unit Constant](../../../../GameMaker_Language/GML_Reference/Time_Sources/Time_Source_Units)  |                                                              |       |
| Constant                                                                                                       | Description                                                  | Value |
|  time_source_units_seconds                                                                                     | Use seconds for the Time Source period (frame-independent)   | 0     |
|  time_source_units_frames                                                                                      | Use frames for the Time Source period (frame-dependent)      | 1     |

These constants are used in [ time_source_create()
](time_source_create) and [ time_source_reconfigure()
](time_source_reconfigure) to set the units used for the Time Source
's period, and are returned by [ time_source_get_units()
](time_source_get_units) . If you use seconds, your Time Source will
run independently from the game's framerate. If you use frames, your
Time Source will be dependent on the game's framerate. You can also use
BPM (beats-per-minute) as a unit by calling [ time_bpm_to_seconds()
](time_bpm_to_seconds) to convert your BPM value to a period in
seconds, and then using time_source_units_seconds as the unit.
