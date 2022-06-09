# audio_group_load

This function will load all the sounds that are flagged as belonging to
the given Audio Group into memory. The function will return true if
loading is initiated and false if the group ID is invalid, or it has
already been flagged for loading. The function is asynchronous so your
game will continue to run while the audio is loaded in the background.
This means that it will also trigger an [Asynchronous Load/Save
Event](../../../../../The_Asset_Editors/Object_Properties/Async_Events/Save_Load)
to inform you that the whole group has been loaded into memory and the
sounds can now be used.

#### Syntax:

``` gml
audio_group_load(groupID);
```

|          |                                                                                                                             |                                                                                                                           |
|----------|-----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                        | Description                                                                                                               |
| groupID  |  [Audio Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/Audio_Groups)  | The index of the audio group to load (as defined in the [Audio Groups Window](../../../../../Settings/Audio_Groups) ) |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !audio_group_is_loaded(audiogroup_level1)
{
    audio_group_load(audiogroup_level1);
}
```

The above code checks to see if an audio group has been loaded and if
not, it loads it.
