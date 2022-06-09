# audio_sound_length

This function will return the length of the given sound in seconds. The
sound can either be a referenced from index for an individual sound
being played which has been stored in a variable when using the [
audio_play_sound() ](audio_play_sound) or [ audio_play_sound_at()
](audio_play_sound_at) functions, or an actual sound asset from the
Asset Browser.

#### Syntax:

``` gml
audio_sound_length(index);
```

|          |                                                                                                                                                                                    |                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument | Type                                                                                                                                                                               | Description                      |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var len;
len = audio_sound_length(snd_Beam);
audio_play_sound(snd_Beam, 1, false);
alarm[0] = room_speed * len;
```

The above code gets the length (in seconds) of the sound indexed in the
variable "snd_Beam", then plays the sound and sets an alarm to go off
when the sound has finished playing using the length of the sound to
calculate the time needed for the alarm.
