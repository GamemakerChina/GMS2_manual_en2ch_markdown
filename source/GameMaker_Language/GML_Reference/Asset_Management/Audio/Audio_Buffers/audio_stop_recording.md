# audio_stop_recording

This function will stop recording on the given recorder channel (the
channel index is returned when you call the function [
audio_start_recording() ](audio_start_recording) ). When you stop
recording, no further [Audio Recording Asynchronous
Events](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Audio_Recording)
will be triggered for the given recorder channel, so you would normally
use this function in the actual asynchronous event to ensure that you
have captured all the data. ** NOTE ** Most platforms **except HTML5**
support recording audio in some form, but that does not mean that all
devices will permit it, even if the platform does, so you should always
check that the [ audio_get_recorder_count()
](audio_get_recorder_count) function returns a value greater than 0
to verify that recording devices are available before using the rest of
the recording functions.

#### Syntax:

``` gml
audio_stop_recording(channel_index);
```

|               |                                                                            |                                            |
|---------------|----------------------------------------------------------------------------|--------------------------------------------|
| Argument      | Type                                                                       | Description                                |
| channel_index |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the recorder channel to stop. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
audio_stop_recording(audio_channel);
```

The above code tells GameMaker to stop recording on the given audio
channel index.
