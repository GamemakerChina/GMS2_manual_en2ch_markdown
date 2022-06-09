# audio_play_sound_on

With this function you can play any sound resource through an emitter,
with any changes to the emitter gain, position, pitch or velocity
affecting how the user hears the final sound being played. You provide
the emitter index to use, the sound index of the sound to be played and
then specify whether the sound is to loop or not. Finally you can assign
a priority, which is then used to determine how sounds are dealt with
when the number of sounds playing is over the limit set by the function
[ audio_channel_num() ](../audio_channel_num) . Lower priority
sounds will be stopped in favour of higher priority sounds, and the
priority value can be any real number (the actual value is arbitrary,
and can be from 0 to 1 or 0 to 100, as GameMaker will prioritize them
the same). Note that when dealing with priority, the *higher* the number
the *higher* the priority, such that a sound with priority 100 will be
favoured over a sound with priority 1. This function will also return a
unique index number for the sound being played which can then be stored
in a variable so that you can then pause it or stop it with the
appropriate functions. This means that if you have multiple instances of
the same sound playing at any one time you can target just one instance
of that sound to deal with using the audio functions.

#### Syntax:

``` gml
audio_play_sound_on(emitter, sound, loop, priority);
```

|          |                                                                                                                                         |                                         |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                                    | Description                             |
| emitter  |  [Audio Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Emitters/audio_emitter_create)  | The index of the emitter to use.        |
| sound    |  [Sound Asset](../../../../../../The_Asset_Editors/Sounds)                                                                          | The index of the sound to use.          |
| loop     |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                            | Flags the sound as looping or not.      |
| priority |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | Set the channel priority for the sound. |

#### Returns:

``` gml
 Sound Instance ID
```

#### Example:

``` gml
if global.SFX
{
    audio_play_sound_on(s_emit, snd_Explode, false, 1);
}
```

The above code checks the global variable "SFX" and if it returns true
then the sound indexed in the variable "snd_Explode" will be played
through the emitter indexed in the variable "s_emit" with a low priority
and no looping.
