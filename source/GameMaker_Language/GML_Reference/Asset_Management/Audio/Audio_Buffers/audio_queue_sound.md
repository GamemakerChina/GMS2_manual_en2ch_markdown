# audio_queue_sound

This function will add the data from a buffer into the audio queue that
you previously created using the function [ audio_create_play_queue()
](audio_create_play_queue) . You specify the queue index to add to,
and the buffer ID to get the data from as well as the position (offset)
within the buffer and the number of bytes to add. Once you have added
audio from a buffer to a queue, the buffer cannot be deleted until you
have first freed the queue using the function [ audio_free_play_queue()
](audio_free_play_queue) , and the buffer properties should match
those of the the queue that you are adding the sound to.

#### Syntax:

``` gml
audio_queue_sound(queueIndex, bufferId, bufferOffset, bufferLength);
```

|              |                                                                                                                                         |                                                                   |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument     | Type                                                                                                                                    | Description                                                       |
| queueIndex   |  [Audio Queue ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Buffers/audio_create_play_queue)  | The index of the queue to add to.                                 |
| bufferId     |  [Buffer ID](../../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                              | The buffer to add to the queue.                                   |
| bufferOffset |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The offset within the source buffer to start from.                |
| bufferLength |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The length of the buffer (the number of the bytes in the buffer). |

#### Returns:

``` gml
N/A
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
