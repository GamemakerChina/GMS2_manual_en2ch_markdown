# audio_is_paused

This function will check the given sound to see if it is currently
paused. The sound can either be a single instance of a sound (the index
for individual sounds being played can be stored in a variable when
using the [ audio_play_sound() ](audio_play_sound) or [
audio_play_sound_at() ](audio_play_sound_at) functions) or a sound
asset, in which case *all* instances of the given sound will be checked
and if any of them are paused the function will return true otherwise it
will return false .

#### Syntax:

``` gml
audio_is_paused(index);
```

|          |                                                                                                                                                                                    |                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                                                                                               | Description                      |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if audio_is_paused(snd_Waterfall)
{
    audio_resume_sound(snd_Waterfall);
}
```

The above code checks to see if the sound indexed in the variable
"snd_Waterfall" is currently paused and if it returns true then the
playing of the sound will be resumed.
