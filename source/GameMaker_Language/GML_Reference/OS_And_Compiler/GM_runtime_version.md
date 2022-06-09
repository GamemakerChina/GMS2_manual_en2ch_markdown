# GM_runtime_version

This constant hold the runtime version number as defined in the
[Preferences](../../../Setting_Up_And_Version_Information/IDE_Preferences/Runtime_Feed_Preferences)
as the runtime being used to build the project. The value is stored as a
string.

#### Syntax:

``` gml
GM_runtime_version;
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
draw_text(32, 32, date_time_string(GM_build_date)); draw_text(32, 64, "v" + GM_version); draw_text(32, 96, "Runtime " + GM_runtime_version);
```

The above code takes the GM date, version and runtime constants and
draws them to the screen.
