# audio_listener_orientation

With this function you can change the orientation of the *listener*
within the 3D audio space. The **look at** direction and **up**
direction are based on the vectors that are resolved from the given
relative x, y and z positions, and default to (0, 0, 1000) for the look
at direction and (0, 1, 0) for the up direction, as shown in the
illustration below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Orientation_Base.png)  
** NOTE ** if you have multiple listeners you should use the function [
audio_listener_set_orientation() ](audio_listener_set_orientation) .
Changing the listener orientation with this function will change how
sound created by audio emitters around the game room are perceived by
the player of your game. In the example below, sounds created by the
emitter when the listener is at the default position would appear to be
coming from below and to the right of the listener, but with the new
position and orientation of the listener they will now be perceived as
coming from *above* and to the right.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Orientation_Example.png)  

#### Syntax:

``` gml
audio_listener_orientation(lookat_x, lookat_y, lookat_z, up_x, up_y, up_z);
```

|          |                                                                            |                                   |
|----------|----------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                       | Description                       |
| lookat_x |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x look vector (default 0).    |
| lookat_y |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y look vector (default 0).    |
| lookat_z |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z look vector (default 1000). |
| up_x     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x up vector (default 0).      |
| up_y     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y up vector (default 1).      |
| up_z     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The z up vector (default 0).      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
xt = x + dcos(direction);
yt = y - dsin(direction);
zt = z - dsin(zdirection);
audio_listener_position(x, y, z)
audio_listener_orientation(xt, yt, zt, 0, 0, 1)
```

The above code use three variables to set the 3D audio listener position
and orientation.
