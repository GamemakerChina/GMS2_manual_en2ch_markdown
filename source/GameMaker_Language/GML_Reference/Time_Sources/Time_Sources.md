# Time Sources

A " Time Source " is a custom timer you create. It runs for a given
period of time, and at the end, it expires. A Time Source (TS) has the
ability to call a custom method ("callback") on expiring.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Time_Sources/time_sources_flow.png)  
It's also able to repeat a certain of amount of times, or forever. Each
repetition of a Time Source is known as a "rep".

## How to Use Time Sources?

Create and start a Time Source that calls a custom method:

-   Call [ time_source_create() ](time_source_create) / [Create Time
    Source](../../../Drag_And_Drop/Drag_And_Drop_Reference/Time_Sources/Create_Time_Source)
    to create a Time Source
    -   Specify whether this inherits from the Global Time Source , the
        Game Time Source or a custom Time Source
    -   Specify the period of time it runs for, and the units used
        (seconds or frames)
    -   Specify a custom method, with an argument array to pass into
        that method
    -   Optionally, specify the number of times it should repeat
        -   By default it runs only once
-   Call [ time_source_start() ](time_source_start) / [Start Time
    Source](../../../Drag_And_Drop/Drag_And_Drop_Reference/Time_Sources/Start_Time_Source)
    to start that Time Source immediately, or call it later when you
    need it to start

Doing this will cause the Time Source to run, and after the specified
period, it will expire and call your specified method.

## Built-In Time Sources

A Time Source can inherit from either of the two built-in Time Source s,
or from a custom Time Source . See: [Built-In Time
Sources](Built_In_Time_Sources)

## Function List

The following functions are used to create and modify Time Source s:

-   [time_source_create](time_source_create)
-   [time_source_destroy](time_source_destroy)
-   [time_source_start](time_source_start)
-   [time_source_stop](time_source_stop)
-   [time_source_pause](time_source_pause)
-   [time_source_reconfigure](time_source_reconfigure)
-   [time_source_reset](time_source_reset)
-   [time_source_get_children](time_source_get_children)
-   [time_source_get_parent](time_source_get_parent)
-   [time_source_get_period](time_source_get_period)
-   [time_source_get_reps_completed](time_source_get_reps_completed)
-   [time_source_get_reps_remaining](time_source_get_reps_remaining)
-   [time_source_get_state](time_source_get_state)
-   [time_source_get_time_remaining](time_source_get_time_remaining)
-   [time_source_get_units](time_source_get_units)
-   [time_source_exists](time_source_exists)

Each get\_\* function will return undefined if the specified Time Source
doesn't exist. The following helper functions are provided for
converting time periods:

-   [time_seconds_to_bpm](time_seconds_to_bpm)
-   [time_bpm_to_seconds](time_bpm_to_seconds)

Also see: [GML Visual - Time
Sources](../../../Drag_And_Drop/Drag_And_Drop_Reference/Time_Sources/Time_Sources_(GML_Visual))

## Constants

The following constants are used with Time Source functions:

-   [Built-In Time Sources](Built_In_Time_Sources)
-   [Time Source Units](Time_Source_Units)
-   [Time Source Expiry Types](Time_Source_Expiry_Types)
-   [Time Source States](Time_Source_States)
