# audio_group_stop_all

This function will stop all sounds from the given audio group that are
currently playing.

#### Syntax:

``` gml
audio_group_stop_all(groupID);
```

|          |                                                                                                                             |                                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                               |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index of the audio group to stop (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if keyboard_check_pressed(vk_space)
{
    audio_group_stop_all(audiogroup_level1);
}
```

The above code checks for the "space" key and then stops all the audio
playing from the given group.
