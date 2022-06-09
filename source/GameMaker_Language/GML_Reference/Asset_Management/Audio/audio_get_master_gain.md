# audio_get_master_gain

With this function you can get the absolute value for the global volume
of all sounds and music for a specific listener. The default listener
index is 0, but you can use the function [ audio_get_listener_info()
](Audio_Listeners/audio_get_listener_info) to get the different
indices available for the target platform. The gain value returned is
based on a linear scale from 0 (silent) to 1 (full volume). Note that on
some platforms you can have a gain of greater than 1, although a value
of 1 is considered "full volume" and anything greater may introduce
audio clipping.

#### Syntax:

``` gml
audio_get_master_gain(listenerIndex);
```

|               |                                                                                                                                                                                                              |                                               |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument      | Type                                                                                                                                                                                                         | Description                                   |
| listenerIndex |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The index of the listener to get the gain of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var num = audio_get_listener_count();
for(var i = 0; i &amp;lt; num; ++i;)
{
    var info = audio_get_listener_info(i);
    var ind = info[? "index"];
    if audio_get_master_gain(ind) != 1
    {
        audio_set_master_gain(info[? "index"], 1);
    }
    ds_map_destroy(info);
}
```

The above code loops through the available listeners, checking to see if
their gain is 1 or not, and if it is not it sets it to 1 for each of
them.
