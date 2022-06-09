# audio_sound_get_pitch

This function can be used to get the get pitch of a given sound. The
sound can either be one referenced from an index for an individual sound
being played which has been stored in a variable when using the [
audio_play_sound() ](audio_play_sound) or [ audio_play_sound_at()
](audio_play_sound_at) functions, or an actual sound asset from the
Asset Browser.

#### Syntax:

``` gml
audio_sound_get_pitch(index);
```

|          |                                                                                                                                                                                    |                                             |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                                                                                                                               | Description                                 |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to get the pitch of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if audio_sound_get_pitch(snd_Explode) != 1
{
    audio_sound_pitch(snd_Explode, 1);
}
```

The above code will change the pitch of the audio played from the sound
indexed as "snd_Explode" if its pitch is not equal to 1.
