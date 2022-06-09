# audio_resume_all

With this function you can resume all sounds that have been paused
previously.

#### Syntax:

``` gml
audio_resume_all();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(ord("P"))
{
    global.Pause = !global.Pause;
    if global.Pause
    {
        audio_pause_all();
    }
    else
    {
        audio_resume_all();
    }
}
```

The above code checks for a press of the keyboard key "P" and if it
detects one it sets the global variable "Pause" to true or false and
then either pauses all sounds or restarts all previously paused sounds.
