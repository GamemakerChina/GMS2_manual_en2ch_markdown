# audio_listener_velocity

This function can be used to give the listener *Doppler* effects and
simulate audio motion based on the vector that is resolved from the
given relative x, y and z positions. If the listener itself is not ever
going to move, or the movement is not a constant motion, you would
normally not need to set these values, but, for example, if you are
making a scrolling game where the player has a constant bottom to top
movement and the enemies a constant top to bottom movement, you would
set the listener *and* emitter velocities (for emitters you would use [
audio_emitter_velocity() ](../Audio_Emitters/audio_emitter_velocity)
) to the appropriate vectors to simulate the correct Doppler effect as
they move past the player instance. ** NOTE ** if you have multiple
listeners you should use the function [ audio_listener_set_velocity()
](audio_listener_set_velocity) . The image below shows how this
could be setup for the example game given above:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Listener_Velocity.png)  

#### Syntax:

``` gml
audio_listener_velocity(vx, vy, vz);
```

|          |                                                                            |                                                       |
|----------|----------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                       | Description                                           |
| vx       |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x velocity component of the listener (default 0). |
| vy       |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y velocity component of the listener (default 0). |
| vz       |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z velocity component of the listener (default 0). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if speed &amp;gt; 0
{
    audio_listener_velocity(abs(hspeed), abs(vspeed), 0);
}
```

The above code checks to see if the player instance speed is over 0 and
if it is it then uses the appropriate absolute hspeed and vspeed
components to set the listener velocity.
