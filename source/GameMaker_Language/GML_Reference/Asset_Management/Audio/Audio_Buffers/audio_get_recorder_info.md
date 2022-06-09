# audio_get_recorder_info

This function will return a [DS
Map](../../../Data_Structures/DS_Maps/DS_Maps) with information
about the given recorder source index. You can find out how many
recorder sources are available using the function [
audio_get_recorder_count() ](audio_get_recorder_count) , and the map
returned will contain the following key/value pairs:

-   " **name** " - a name to describe the device
-   " **index** " - the index to be used to record
-   " **data_format** " - the format data will be returned in (this is
    currently always buffer_s16 but other formats may be supported in
    the future)
-   " **sample_rate** " - the sample rate (in Hz) of the data returned
    (currently clamped to 16000hz but this may change in future)
-   " **channels** " - the constant audio_mono (further constants for
    stereo and 3D may be supported in the future)

Note that while the function creates a DS map for you, it does *not*
remove it again later and so you should be destroying the map yourself
when it is no longer needed to prevent any memory leaks. ** NOTE ** Most
platforms **except HTML5** support recording audio in some form, but
that does not mean that all devices will permit it, even if the platform
does, so you should always check that the [ audio_get_recorder_count()
](audio_get_recorder_count) function returns a value greater than 0
to verify that recording devices are available before using the rest of
the recording functions.

#### Syntax:

``` gml
audio_get_recorder_info(recorder_index);
```

|                |                                                                            |                                                               |
|----------------|----------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument       | Type                                                                       | Description                                                   |
| recorder_index |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The index of the recorder source to get the information from. |

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
len = async_load[? "data_len"];
audio_buff = buffer_create(len, buffer_fast, 1);
buffer_copy(async_load[? "buffer_id"], 0, len, buff, 0);
audio_queue_sound(audio_queue, audio_buff, 0, len);
audio_play_sound(audio_queue, 10, 0);
```

The above code would be called in the asynchronous [Audio
Recording](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Audio_Recording)
event and assigns some recorded data to a buffer, which is then added to
an audio queue. This is then played.
