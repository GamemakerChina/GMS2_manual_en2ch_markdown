# audio_destroy_stream

If you have previously created an audio stream from a file using the
function [ audio_create_stream() ](audio_create_stream) and no
longer need that sound, you can call this function to delete it from
memory. Any further calls to the sound index after it has been destroyed
will give an error. It should be noted that this will free up the stream
but on the target platform this may not show up in a memory manager.
This is because GameMaker pools memory resources to prevent memory
allocation overhead, and so the memory will remain allocated until
required for something else or re-used for a new stream. **NOTE** : This
functionality is not available for the HTML5 target platform.

#### Syntax:

``` gml
audio_destroy_stream(filename);
```

|          |                                                                           |                                           |
|----------|---------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                      | Description                               |
| filename |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Path to the audio file that was streamed. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
audio_destroy_stream(snd);
```

The above code removes the sound indexed in the variable "snd" from
memory.
