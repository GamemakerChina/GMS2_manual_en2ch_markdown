# uwp_license_trial_time_remaining

This function will return the approximate number of seconds until a
time-based trial expires. The value returned by this function is
meaningless if the trial is not time-based or if the game is not running
in trial mode.

#### Syntax:

``` gml
uwp_license_trial_time_remaining();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if uwp_license_trial_version()
{
    var secs = uwp_license_trial_time_remaining() mod 60;
    var mins = uwp_license_trial_time_remaining() div 60;
    var hours = mins div 60;
    if secs &amp;lt; 10 secs = "0" + string(secs) else secs = string(secs);
    if mins &amp;gt; 60 mins -= (hours * 60);
    if mins &amp;lt; 10 mins = "0" + string(mins) else mins = string(mins);
    if hours &amp;gt; 9 hours = "9" else hours = string(hours);
    time_string = hours + ":" + mins + ":" + secs;
}
```

The above code checks to see if the game is being run with a trial
licence and if it is it creates a string with the time until the licence
expires.
