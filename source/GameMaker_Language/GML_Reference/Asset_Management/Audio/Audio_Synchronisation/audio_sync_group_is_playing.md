# audio_sync_group_is_playing

This function can be used to check if any audio in a synchronised group
is playing. You are required to supply the sync group ID as returned by
the function [ audio_create_sync_group() ](audio_create_sync_group)
. **NOTE** : This functionality is not available for the HTML5 target
platform.

#### Syntax:

``` gml
audio_sync_group_is_playing(group_index);
```

|             |                                                                                                                                                      |                           |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| Argument    | Type                                                                                                                                                 | Description               |
| group_index |  [Audio Sync Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Synchronisation/audio_create_sync_group)  | The group index to check. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if audio_sync_group_is_playing(group_one)
{
    audio_stop_sync_group(group_one);
}
```

The above code checks to see if the sync group group_one is currently
playing and if it is, the group is stopped.
