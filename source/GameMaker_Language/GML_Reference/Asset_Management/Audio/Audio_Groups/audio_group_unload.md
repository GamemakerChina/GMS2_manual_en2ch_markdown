# audio_group_unload

This function will unload all the sounds that are flagged as belonging
to the given Audio Group into memory. The function will return true if
unloading is initiated and false if the group ID is invalid, or it has
already been flagged for unloading. Note that any audio currently being
played when this function is called will be stopped.

#### Syntax:

``` gml
audio_group_unload(groupID);
```

|          |                                                                                                                             |                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                                 |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index of the audio group to unload (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |

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
