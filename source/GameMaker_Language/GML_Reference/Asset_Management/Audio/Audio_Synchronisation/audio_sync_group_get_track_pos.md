# audio_sync_group_get_track_pos

This function returns the current play position of the given sync group.
The group index is the value returned when you created the group using
the function [ audio_create_sync_group() ](audio_create_sync_group)
, and the return value is the time in seconds that the tracks have been
playing. **NOTE** : This functionality is not available for the HTML5
target platform.

#### Syntax:

``` gml
audio_sync_group_get_track_pos(group_index);
```

|             |                                                                                                                                                      |                                         |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument    | Type                                                                                                                                                 | Description                             |
| group_index |  [Audio Sync Group ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Synchronisation/audio_create_sync_group)  | The group index to get the position of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var real_secs = audio_sync_group_get_track_pos(sg);
var secs = real_secs mod 60;
var mins = string(real_secs div 60);
if (secs &amp;gt; 9)
{
    secs = string(secs);
}
else
{
    secs = "0" + string(secs);
}

draw_text(32, 32, "Time = " + mins + ":" + secs);
```

The above code gets the time position for the sync group indexed in the
variable "sg", then uses this value to draw the time played on the
screen.
