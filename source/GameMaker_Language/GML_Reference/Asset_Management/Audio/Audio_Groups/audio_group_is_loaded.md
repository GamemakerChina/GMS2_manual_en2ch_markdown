# audio_group_is_loaded

This function will check a specific audio group to see if it has been
loaded into memory, ready for use.

#### Syntax:

``` gml
audio_group_is_loaded(groupID);
```

|          |                                                                                                                             |                                                                                                                            |
|----------|-----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                                |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index of the audio group to check (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if audio_group_is_loaded(audiogroup_level1)
{
    audio_group_unload(audiogroup_level1);
}
```

The above code checks to see if an audio group has been loaded and if it
has it unloads it.
