# audio_group_set_gain

With this function you can fade a group of sounds in or out over a given
length of time, or it can be used to set the group gain instantly. The
time is measured in milliseconds, and the function requires that you
input a final level of gain for the group to have reached by the end of
that time. This gain can be between 0 (silent) and 1 (full volume) and
the scale is linear, such that a value of 0.5 would be half volume. To
instantly change the gain, simply set the time argument to 0. Note that
on some platforms you can have a gain of greater than 1, although a
value of 1 is considered "full volume" and anything greater may
introduce audio clipping.

#### Syntax:

``` gml
audio_group_set_gain(groupID, volume, time);
```

|          |                                                                                                                             |                                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                               |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index of the audio group to stop (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |
| volume   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | The final value for the group volume.                                                                                     |
| time     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | The length of the change in gain in milliseconds.                                                                         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(vk_space)
{
    audio_group_set_gain(audiogroup1, 0, 5000);
}
```

The above code checks for the "space" key and then fades all the audio
for "audiogroup1" down to 0 over 5 seconds.
