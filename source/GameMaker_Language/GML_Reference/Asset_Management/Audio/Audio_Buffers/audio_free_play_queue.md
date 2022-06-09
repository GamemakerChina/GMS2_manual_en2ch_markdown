# audio_free_play_queue

This function is used to free up the memory associated with the given
audio queue. The queue index is the value returned when you created the
queue using the function [ audio_create_play_queue()
](audio_create_play_queue) , and this function should be called when
the queue is no longer required to prevent memory leaks. Freeing the
queue will stop any sound that is be playing, and you cannot delete the
buffer that a sound is being streamed from until the queue it is
assigned to has been freed. This function will trigger an [Audio
Playback Asynchronous
Event](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Audio_Playback)
, and in this event a special [DS
map](../../../Data_Structures/DS_Maps/DS_Maps) will be created in
the variable [ async_load
](../../../../GML_Overview/Variables/Builtin_Global_Variables/async_load)
with the following key/value pairs:

-   " **queue_id** " - the queue that has finished playing data
-   " **buffer_id** " - the buffer that is no longer being played from
-   " **queue_shutdown** " - this is set to 0 during normal playback and
    1 when the event is received because you have freed the queue with
    this function. When this is set to 1, you don't want to queue up any
    further data.

#### Syntax:

``` gml
audio_free_play_queue(queueIndex);
```

|            |                                                                                                                                         |                                 |
|------------|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument   | Type                                                                                                                                    | Description                     |
| queueIndex |  [Audio Queue ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Buffers/audio_create_play_queue)  | The index of the queue to free. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var q_id = async_load[? "queue_id"];
if (q_id == audio_queue)
{
    audio_free_play_queue(audio_queue);
    buffer_delete(audio_buffer);
}
```

The above code would go in the asynchronous [Audio
Playback](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Audio_Playback)
event and checks to see if the audio that has finished playing is from
the "audio_queue" and if it is it frees the queue and the buffer
associated with it.
