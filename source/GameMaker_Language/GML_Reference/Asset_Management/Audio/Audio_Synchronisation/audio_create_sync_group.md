# audio_create_sync_group

Creates a sync group and returns a unique ID value for it which should
then be used in all further audio function calls for this group. If you
want the group to loop then pass in true , otherwise pass in false , but
note that if you want them to loop, *all the tracks added later need to
be the same length* . Note that when you create a sync group, you will
need to free the memory and sounds associated with it when not in use
using the [ audio_destroy_sync_group() ](audio_destroy_sync_group)
function - for example, in the **Room End** or **Destroy** events.
**NOTE** : This functionality is not available for the HTML5 target
platform.

#### Syntax:

``` gml
audio_create_sync_group(loop);
```

|          |                                                                               |                                                                            |
|----------|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                          | Description                                                                |
| loop     |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the tracks in the group should loop ( true ) or not ( false ).     |

#### Returns:

``` gml
 Audio Sync Group ID
```

#### Example:

``` gml
sg = audio_create_sync_group(true);
audio_play_in_sync_group(sg, sound1);
audio_play_in_sync_group(sg, sound2);
audio_sound_gain(sound2, 0, 0);
audio_play_in_sync_group(sg, sound3);
audio_sound_gain(sound3, 0, 0);
audio_play_in_sync_group(sg, sound4);
audio_sound_gain(sound4, 0, 0);
audio_start_sync_group(sg);
```

The above creates a new sync group and assigns the index of the group to
the variable "sg". Four sounds are then added to the group, with the
gain for three of them set to 0. Finally the sync group is played.
