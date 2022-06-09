# audio_start_recording

This function will start recording audio from the recorder source
indexed. You can get the number of recorder sources using the function [
audio_get_recorder_count() ](audio_get_recorder_count) , and once
you start recording the audio will be stored in a temporary buffer and
start triggering an [Audio Recording Asynchronous
Event](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Audio_Recording)
. This event is triggered every step that recording takes place and will
create the special [DS
map](../../../Data_Structures/DS_Maps/DS_Maps) in the variable [
async_load
](../../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
with the following key/value pairs:

-   " **buffer_id** " - the ID of the temporary buffer you can use to
    retrieve the audio data
-   " **channel_index** " - the recording channel index (as returned by
    the function) this data came from
-   " **data_len** " - the length of data (in bytes) you've received

Note that after the asynchronous event has been triggered, the audio in
the temporary buffer will be wiped, so you should be copying it's data
into a custom buffer that you have previously created. ** NOTE ** Most
platforms **except HTML5** support recording audio in some form, but
that does not mean that all devices will permit it, even if the platform
does, so you should always check that the [ audio_get_recorder_count()
](audio_get_recorder_count) function returns a value greater than 0
to verify that recording devices are available before using the rest of
the recording functions.

#### Syntax:

``` gml
audio_start_recording(recorder_index);
```

|                |                                                                            |                                          |
|----------------|----------------------------------------------------------------------------|------------------------------------------|
| Argument       | Type                                                                       | Description                              |
| recorder_index |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the recorder source to use. |

#### Returns:

``` gml
 Buffer ID
```

#### Example:

``` gml
audio_record = audio_start_recording(0);
```

The above code starts recording from the recorder source 0, storing the
channel index of the recording in the variable "audio_record" for use in
the asynchronous [Audio
Recording](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Audio_Recording)
event.
