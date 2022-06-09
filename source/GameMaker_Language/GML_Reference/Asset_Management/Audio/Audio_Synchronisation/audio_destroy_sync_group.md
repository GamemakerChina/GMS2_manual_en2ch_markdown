# audio_destroy_sync_group

Audio sync groups need to be destroyed when not in use to free up the
memory and sound resources associated with them using this function. It
takes the group index as returned when the group was created using the
function [ audio_create_sync_group() ](audio_create_sync_group) ,
and frees all resources used by the group. **NOTE** : This functionality
is not available for the HTML5 target platform.

#### Syntax:

``` gml
audio_destroy_sync_group(group_index);
```

|             |                                                                                                                                                      |                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument    | Type                                                                                                                                                 | Description                      |
| group_index |  [Audio Sync Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Synchronisation/audio_create_sync_group)  | The group index to be destroyed. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
audio_destroy_sync_group(sg);
```

The above code destroys the sync group indexed in the variable "sg", and
would probably be used in the **destroy** or **Room End** events.
