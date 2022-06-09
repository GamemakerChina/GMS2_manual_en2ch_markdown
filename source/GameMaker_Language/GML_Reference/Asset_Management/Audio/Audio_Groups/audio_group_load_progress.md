# audio_group_load_progress

This function will check the loading progress for an audio group and
return an (approximate) value between 0 and 100.

#### Syntax:

``` gml
audio_group_load_progress(groupID);
```

|          |                                                                                                                             |                                                                                                                            |
|----------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                                |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index of the audio group to check (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if load
{
    var pc = audio_group_load_progress(audiogroup_level1);
    draw_text(32, 32, "Loading: " + string(pc));
}
```

The above code checks a variable and if it returns true then some text
will be drawn showing the progress of the audio being loaded.
