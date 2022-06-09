# audio_create_buffer_sound

With this function you can create a new sound from the contents of a
buffer. The buffer will have been created previously (see the [buffer
functions](../../../Buffers/Buffers) for details on how to do this),
and have had data added or loaded into it. You then pass it to this
function with the data format (only buffer_u8 or buffer_s16 are
currently supported), the sample rate (which can be between 1000hz and
48000hz), and an offset into the buffer to get the data from. You also
need to supply the number of samples in the buffer and the channels that
the sound requires. These channels are defined by one of the following
constants:

|                                                                                                                                                   |                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------|
|  [Audio Channel Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Buffers/audio_create_buffer_sound)  |                              |
| Constant                                                                                                                                          | Description                  |
|  audio_mono                                                                                                                                       | Mono (single channel) audio. |
|  audio_stereo                                                                                                                                     | Stereo (dual channel) audio. |
|  audio_3D                                                                                                                                         | 3D (5.1) audio.              |

Note that after you have created a sound, you should free the pointer
index associated with it when it is no longer required using the
function [ audio_free_buffer_sound() ](audio_free_buffer_sound) . If
you fail to do this and then re-assign the variable or change rooms
etc... the sound ID will be lost and you will have a memory leak. Also
note that you cannot delete the buffer if any sound has been created
from it and the sound has not been freed up first. So you would free the
sound (or sounds) first, *then* delete the buffer. It is also worth
noting that adding anything to the buffer, or changing the buffer size,
after it has had a sound created from it will give unexpected results
and it is not recommended - once you have started creating sounds from
any buffer you should not manipulate it in any other way afterwards.

#### Syntax:

``` gml
audio_create_buffer_sound(bufferId, bufferFormat, bufferRate, bufferOffset, bufferLength, bufferChannels);
```

|                |                                                                                                                                                   |                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Argument       | Type                                                                                                                                              | Description                                                                         |
| bufferId       |  [Buffer ID](../../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_create)                                                        | The ID of the buffer to use.                                                        |
| bufferFormat   |  [Buffer Data Type Constant](../../../../../../GameMaker_Language/GML_Reference/Buffers/buffer_write)                                         | The format of the data in the buffer ( buffer_u8 or buffer_s16 ).                   |
| bufferRate     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | The sample rate of the data in the buffer.                                          |
| bufferOffset   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | The offset into the buffer to read the sample data from (in bytes).                 |
| bufferLength   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                         | The length of the buffer (the number of bytes of audio data, excluding the header). |
| bufferChannels |  [Audio Channel Constant](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Buffers/audio_create_buffer_sound)  | The channels to use from one of the constants listed above.                         |

#### Returns:

``` gml
 Sound Asset
```

#### Example:

``` gml
var rate = 44100;
var hertz = irandom_range(220, 880);
var samples = 44100;

var bufferId = buffer_create(rate, buffer_fast, 1);
buffer_seek(bufferId, buffer_seek_start, 0);

var num_to_write = rate / hertz;
var length = buffer_get_size(bufferId);
var val_to_write = 1;

for (var i = 0; i &amp;lt; (samples / num_to_write) + 1; i++)
{
    for (var j = 0; j &amp;lt; num_to_write; j++)
    {
        buffer_write(bufferId, buffer_u8, val_to_write * 255);
    }
    val_to_write = (1 - val_to_write);
}

soundId = audio_create_buffer_sound(bufferId, buffer_u8, rate, 0, length, audio_stereo);
```

The above creates a buffer and then procedurally fills it with data.
This data is then used to create a new sound, which is stored in the
variable "soundId".
