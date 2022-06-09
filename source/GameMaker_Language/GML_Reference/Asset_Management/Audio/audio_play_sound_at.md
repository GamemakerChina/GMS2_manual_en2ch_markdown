# audio_play_sound_at

With this function you can play any sound resource at a given position
within the audio space. You provide the sound index and then assign it a
position within the 3D space. The default listener position is (0, 0, 0)
so this means that if the listener has not been moved and you want the
sound to come from the left (for example), you should set the x position
to a negative value (for more information on setting the listener
position see [ audio_listener_position()
](Audio_Listeners/audio_listener_position) ). You can also set a
fall-off distance (0 will make the sound silent, default is 100) which
will make the sound fade out as it gets further from the listener
position. How the fade itself is heard will depend on the falloff
reference (which is the distance under which the volume for the source
would normally drop by half) and the roll off factor (which affects the
sound past the falloff reference distance only). The default factor is
normally 1, and the effect of the different falloff values will depend
on the model chosen (for a complete guide to the different falloff
models and how these values are used, please see the function [
audio_falloff_set_model() ](audio_falloff_set_model) ). The last two
arguments are to set the sound is to loop or not and, finally, for
assigning a priority to the sound. This priority is then used to
determine how sounds are dealt with when the number of sounds playing is
over the limit set by the function [ audio_channel_num()
](audio_channel_num) . Lower priority sounds will be stopped in
favour of higher priority sounds, and the priority value can be any real
number (the actual value is arbitrary, and can be from 0 to 1 or 0 to
100, as GameMaker will prioritize them the same). Note that when dealing
with priority, the *higher* the number the *higher* the priority, such
that a sound with priority 100 will be favoured over a sound with
priority 1. This function will return a unique index number for the
sound being played which can then be stored in a variable so that you
can then pause it or stop it with the appropriate functions. This means
that if you have multiple instances of the same sound playing at any one
time you can target just one instance of that sound to deal with using
the audio functions.

#### Syntax:

``` gml
audio_play_sound_at(index, x, y, z, falloff_ref, falloff_max, falloff_factor, loop, priority);
```

|                |                                                                            |                                                         |
|----------------|----------------------------------------------------------------------------|---------------------------------------------------------|
| Argument       | Type                                                                       | Description                                             |
| index          |  [Sound Asset](../../../../../The_Asset_Editors/Sounds)                | The index of the sound to play.                         |
| x              |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x position.                                         |
| y              |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y position.                                         |
| z              |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The z position.                                         |
| falloff_ref    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The falloff reference relative to the listener (clamp). |
| falloff_max    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The maximum falloff distance relative to the listener.  |
| falloff_factor |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The falloff factor (default 1).                         |
| loop           |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Flags the sound as looping or not.                      |
| priority       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | Set the channel priority for the sound.                 |

#### Returns:

``` gml
 Sound Instance ID
```

#### Example:

``` gml
if global.SFX
{
    audio_play_sound_at(snd_Waterfall, x, y, 0, 100, 300, 1, true, 1);
}
```

The above code checks the global variable "SFX" and if it returns true
then the sound indexed in the variable "snd_Waterfall" will be looped at
its room position, with a fall-off reference of 100, a falloff distance
of 300, a falloff factor of 1 and a low priority.
