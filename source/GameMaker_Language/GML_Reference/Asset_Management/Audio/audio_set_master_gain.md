# audio_set_master_gain

With this function you can set the absolute value for the global volume
of all sounds and music for a specific listener. The default listener
index is 0, but you can use the function
[audio_get_listener_info()](Audio_Listeners/audio_get_listener_info)
to get the different indices available for the target platform. The gain
value is based on a linear scale from 0 (silent) to 1 (full volume) and
will affect the relative volume of all sounds and music played from
within your game through that listener.

#### Syntax:

``` gml
audio_set_master_gain(listenerIndex, gain);
```

|               |                                                                                                                                                                                                              |                                               |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Argument      | Type                                                                                                                                                                                                         | Description                                   |
| listenerIndex |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The index of the listener to set the gain on. |
| gain          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                       | Value for the global volume (0 to 1).         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var num = audio_get_listener_count();
for( var i = 0; i &amp;lt; num; i++;)
{
    var info = audio_get_listener_info(i);
    audio_set_master_gain(info[? "index"], 0.75);
    ds_map_destroy(info);
}
```

The above code loops through the available listeners and then sets their
master gain to 0.75.
