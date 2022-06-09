# audio_sound_is_playable

This function can be used to check if the given sound index can be
played currently. This is needed due to the different ways streamed and
unstreamed sound playback is handled on the **HTML5** target platform,
and will return true if the sound can be played and false if it can't.
Note that on all other platforms other than HTML5, the function will
always return true .

#### Syntax:

``` gml
audio_sound_is_playable(index);
```

|          |                                                              |                                  |
|----------|--------------------------------------------------------------|----------------------------------|
| Argument | Type                                                         | Description                      |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds)  | The index of the sound to check. |

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
