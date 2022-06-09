# Save / Load

  
![](https://gms.magecorn.com/Manual/assets/Images/Asset_Editors/Async_SaveLoad.png)  
This event will be triggered by the callback from certain functions
related to loading and saving buffers to files, as well as when loading
or unloading audio from memory. The event itself will contain the built
in [ async_load
](../../../GameMaker_Language/GML_Overview/Variables/Builtin_Global_Variables/async_load)
DS map which will be populated by the keys required for the specific
function. These are listed in the sections below.

## Buffers

When you use the functions [ buffer_save_async()
](../../../GameMaker_Language/GML_Reference/Buffers/buffer_save_async)
or [ buffer_load_async()
](../../../GameMaker_Language/GML_Reference/Buffers/buffer_load_async)
an asynchronous event will be triggered when the data transfer has been
completed. This event will populate the async_load map with the
following key/value pairs

-   " id ": the ID of the async function as returned by the function
    used.
-   " status ": will return true if the data was saved/loaded correctly,
    and false otherwise.

This permits you to poll the saving/loading progress and display a
message or change rooms etc... when the process is complete.

## Audio Groups

When working with [Audio Groups](../../../Settings/Audio_Groups) ,
you can load them an unload them from memory using the functions [
audio_group_load()
](../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/audio_group_load)
and [ audio_group_unload()
](../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Groups/audio_group_unload)
. When using the load function, it will trigger this event when the full
set of audio files set for the group has been loaded into memory and
will populate the map with the following key/value pairs:

-   " type ": this tells us the type of event being called and will be
    "audiogroup_load" for loading audio.
-   " group_id ": will return the ID of the audio group that has been
    loaded (as defined in the [Audio Group
    Editor](../../../Settings/Audio_Groups) ).

When all audio has been loaded for a group, this event will trigger and
it can then be used to change rooms, or play a music track etc...
