# audio_is_playing

This function will check the given sound to see if it is currently
playing. The sound can either be a single instance of a sound (the index
for individual sounds being played can be stored in a variable when
using the [ audio_play_sound() ](audio_play_sound) or [
audio_play_sound_at() ](audio_play_sound_at) functions) or a sound
asset, in which case *all* instances of the given sound will be checked
and if any of them are playing the function will return true otherwise
it will return false . Note that this function will still return true if
the sound being checked has previously been paused using the [
audio_pause_sound() ](audio_pause_sound) function.

#### Syntax:

``` gml
audio_is_playing(index);
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
if !audio_is_playing(snd_Waterfall)
{
    audio_play_sound_at(snd_Waterfall, x, y, 0, 300, true, 1);
}
```

The above code checks to see if the sound indexed in the variable
"snd_Waterfall" is currently playing and if it returns false then the
sound will be looped at its room position, with a fall-off distance of
300 and a low priority.
