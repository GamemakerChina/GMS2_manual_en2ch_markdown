# audio_stop_sound

This function will stop the given sound if it is currently playing. The
sound can either be a single instance of a sound (the index for
individual sounds being played can be stored in a variable when using
the [ audio_play_sound() ](audio_play_sound) or [
audio_play_sound_at() ](audio_play_sound_at) functions) or a sound
asset, in which case *all* instances of the given sound will be stopped.

#### Syntax:

``` gml
audio_stop_sound(index);
```

|          |                                                                                                                                                                                    |                                 |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                                                                                               | Description                     |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to stop. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !global.SFX
{
    audio_stop_sound(snd_Waterfall);
}
else
{
    audio_play_sound_at(snd_Waterfall, x, y, 0, 100, 300, 1, true, 1);
}
```

The above code checks the global variable "SFX" and if it returns false
, it will stop the sound indexed in the variable "snd_Waterfall" that is
currently playing, and if it returns true , it will loop the sound.
