# audio_create_stream

With this function you can create a new sound index which can then be
used in the regular audio functions to stream audio directly from an
external OGG file source. The function requires the filename (which can
be an included file, for example) and will return the new sound index
for use. Note that after you no longer need the sound you should call
the function [ audio_destroy_stream() ](audio_destroy_stream) with
the sound index to remove it from memory otherwise you may get a memory
leak which will slow down and eventually crash your game. **NOTE** :
This functionality is not available for the HTML5 target platform.

#### Syntax:

``` gml
audio_create_stream(filename);
```

|          |                                                                           |                                                       |
|----------|---------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                      | Description                                           |
| filename |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Path to the file (OGG only) to stream the audio from. |

#### Returns:

``` gml
 Sound Asset
```

#### Example:

``` gml
snd = audio_create_stream("Music/Track1.ogg");
audio_play_sound(snd, 0, true);
```

The above code creates a new sound index in the variable "snd" from the
given file, then plays this sound.
