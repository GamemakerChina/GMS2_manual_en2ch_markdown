# audio_get_recorder_count

This function will return the number of audio recording sources (like
microphones, etc...) currently available to your game. So, if you have a
return value of, for example, four, then you will have audio input on
the sources 0, 1, 2 and 3, with one of these values being that which you
use to start recording from using the function [ audio_start_recording()
](audio_start_recording) . This value can change at any time as
people plug/unplug microphones or other input sources to the device.
Note that you can use the function [ audio_get_recorder_info()
](audio_get_recorder_info) to get information on each device
connected. **IMPORTANT!** This function will always return 0 when used
on the HTML5 target.

#### Syntax:

``` gml
audio_get_recorder_count();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if audio_get_recorder_count() &amp;gt; 0
{
    channel_index = audio_start_recording(0);
}
```

The above code checks the audio recorders available and if there are 1
or more, it starts recording from the first one indexed (source 0).
