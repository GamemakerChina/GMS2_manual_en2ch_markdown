# audio_listener_set_velocity

This function can be used to give the given listener *Doppler* effects
and simulate audio motion based on the vector that is resolved from the
given relative x, y and z positions. The default listener index is 0,
but you can use the function [ audio_get_listener_info()
](audio_get_listener_info) to get the different indices available
for the target platform. If the given listener is not ever going to
move, or the movement is not a constant motion, you would normally not
need to set these values, but, for example, if you are making a
scrolling game where the player has a constant bottom to top movement
and the enemies a constant top to bottom movement, you would set the
listener *and* emitter velocities (for emitters you would use [
audio_emitter_velocity() ](../Audio_Emitters/audio_emitter_velocity)
) to the appropriate vectors to simulate the correct Doppler effect as
they move past the player instance. The image below shows how this could
be setup for the example game given above:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Listener_Velocity.png)  

#### Syntax:

``` gml
audio_listener_set_velocity(index, x, y, z);
```

|          |                                                                                                                                                                                                                    |                                                     |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                                                                                                                               | Description                                         |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The listener to change the velocity of (default 0). |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The x velocity of the listener (default 0).         |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The y velocity of the listener (default 0).         |
| z        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The z velocity of the listener (default 0).         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var num = audio_get_listener_count();
for(var i = 0; i &amp;lt; num; ++i;)
{
    var info = audio_get_listener_info(i);
    var data = audio_listener_get_data(info[? "index"]);
    if data[? "vx"] != 0
    {
        audio_listener_set_velocity(info[? "index"], 0, 0, 0);
    }
    ds_map_destroy(info);
    ds_map_destroy(data);
}
```

The above code checks the number of listeners available then loops
through them and if their x velocity is not 0, it sets their velocity
values to 0, 0, 0.
