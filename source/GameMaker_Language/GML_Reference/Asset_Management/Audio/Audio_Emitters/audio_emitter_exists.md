# audio_emitter_exists

This function returns whether an audio emitter exists ( true ) or not (
false ). Note that if the index you search for has not been initialised
previously, this function will cause an error as it is searching for
non-existent indices.

#### Syntax:

``` gml
audio_emitter_exists(index);
```

|          |                                                                                                                                         |                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                                                    | Description                                         |
| index    |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to check the existence of. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if audio_emitter_exists(s_emit)
{
    audio_play_sound_on(s_emit, snd_Explode, false, 1);
}
else
{
    s_emit = audio_emitter_create();
    audio_play_sound_on(s_emit, snd_Explode, false, 1);
}
```

The above code checks to see if an emitter exists, indexed in the
(previously initialised) variable "s_emit". If it does then a sound is
played through it, but if it does not, it is created and then the sound
is played.
