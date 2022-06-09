# audio_sound_get_gain

This function will return the current gain value for the given sound.
The sound can either be one referenced from an index for an individual
sound being played which has been stored in a variable when using the [
audio_play_sound() ](audio_play_sound) or [ audio_play_sound_at()
](audio_play_sound_at) functions, or an actual sound asset from the
Asset Browser. Gain is usually calculated as a value from 0 to 1, but on
some platforms you can have a gain of greater than 1, although a value
of 1 is considered "full volume" and anything greater may introduce
audio clipping.

#### Syntax:

``` gml
audio_sound_get_gain(index);
```

|          |                                                                                                                                                                                    |                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                                                                                                                               | Description                                |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to get the gain of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if audio_sound_get_gain(snd_Music) != 1
{
    audio_sound_gain(snd_Music, 1, 0);
}
```

The above code will change the gain of the audio played from the sound
indexed as "snd_Music" if its gain is not equal to 1.
