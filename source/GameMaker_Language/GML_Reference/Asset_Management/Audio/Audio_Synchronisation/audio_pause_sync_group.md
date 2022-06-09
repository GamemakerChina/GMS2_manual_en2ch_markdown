# audio_pause_sync_group

his function will pause the given sync group if it is playing, with the
group index being the value returned when you created the group using
the function [ audio_create_sync_group() ](audio_create_sync_group)
. This does not stop the sound, and calling [ audio_resume_sync_group()
](audio_resume_sync_group) , will start it playing from the same
position it was paused at again. **NOTE** : This functionality is not
available for the HTML5 target platform.

#### Syntax:

``` gml
audio_pause_sync_group(group_index);
```

|             |                                                                                                                                                      |                           |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| Argument    | Type                                                                                                                                                 | Description               |
| group_index |  [Audio Sync Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Synchronisation/audio_create_sync_group)  | The group index to pause. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (keyboard_check_pressed((ord)"P"))
{
    global.Pause = !global.Pause
    if global.Pause
    {
        audio_pause_sync_group(sg);
    }
    else
    {
        audio_resume_sync_group(sg);
    }
}
```

The above code checks for a key press of the "P" key, and if one is
detected it toggles the "global.Pause" variable then checks it to pause
or resume the sync group indexed in the variable "sg".
