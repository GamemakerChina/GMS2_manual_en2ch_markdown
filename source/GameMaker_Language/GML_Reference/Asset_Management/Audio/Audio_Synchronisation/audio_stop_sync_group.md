# audio_stop_sync_group

This function will stop the given sync group if it is playing, with the
group index being the value returned when you created the group using
the function [ audio_create_sync_group() ](audio_create_sync_group)
. **NOTE** : This functionality is not available for the HTML5 target
platform.

#### Syntax:

``` gml
audio_stop_sync_group(group_index);
```

|             |                                                                                                                                                      |                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| Argument    | Type                                                                                                                                                 | Description                      |
| group_index |  [Audio Sync Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Synchronisation/audio_create_sync_group)  | The group index to stop playing. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    audio_stop_sync_group(sg);
}
```

The above code checks for a mouse click, and if one is detected it stops
the sync group indexed in the variable "sg".
