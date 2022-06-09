# audio_sound_gain

With this function you can fade a sound in or out over a given length of
time, or it can be used to set the sound gain instantly. The time is
measured in milliseconds, and the function requires that you input a
final level of gain for the sound to have reached by the end of that
time. This gain can be between 0 (silent) and any value greater than 0,
although normally you'd consider the maximum volume as 1. Anything over
1 can be used but, depending on the sound used and the platform being
compiled to, you may get distortion or clipping when the sound is played
back. Note that the gain scale is linear, and to instantly change the
gain, simply set the time argument to 0. This function will affect *all*
instances of the sound that are playing currently in the room if the
index is a sound resource, and the final volume will be the volume at
which all further instances of the sound will be played. However if you
have used the index returned from a function like [ audio_play_sound()
](audio_play_sound) it will only affect that one instance of the
sound.

#### Syntax:

``` gml
audio_sound_gain(index, volume, time);
```

|          |                                                                                                                                                                                    |                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                                                                                                                               | Description                                        |
| index    |  [Sound Asset](../../../../../The_Asset_Editors/Sounds) or [Sound Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/audio_play_sound)    | The index of the sound to set the gain for.        |
| volume   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                             | Value for the music volume.                        |
| time     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                             | The length for the change in gain in milliseconds. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if val
{
    var snd = audio_play_sound(snd_fountain);
    audio_sound_gain(snd, 0, 0);
    audio_sound_gain(snd, 1, 5000);
}
```

The above code checks a variable and if it returns true it will then
assign the index of a sound to be played to the local variable "snd".
This variable is then used to reduce the volume of that specific sound
to 0 and fade up to full volume over 5 seconds.
