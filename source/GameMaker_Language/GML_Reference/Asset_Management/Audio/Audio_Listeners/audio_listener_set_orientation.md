# audio_listener_set_orientation

With this function you can change the orientation of the given
*listener* within the 3D audio space. The default listener index is 0,
but you can use the function [ audio_get_listener_info()
](audio_get_listener_info) to get the different indices available
for the target platform. The **look at** vector and **up** vector are
based on the values that are resolved from the given relative x, y and z
positions, and default to (0, 0, -1) for the look at vector and (0, 1,
0) for the up vector, as shown in the illustration below:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Orientation_Base.png)  
Changing the given listener orientation with this function will change
how sound created by audio emitters around the game room are perceived
by the player of your game. In the example below, sounds created by the
emitter when the listener is at the default position would appear to be
coming from below and to the right of the listener, but with the new
position and orientation of the listener they will now be perceived as
coming from *above* and to the right.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Orientation_Example.png)  

#### Syntax:

``` gml
audio_listener_set_orientation(index, lookat_x, lookat_y, lookat_z, up_x, up_y, up_z);
```

|          |                                                                                                                                                                                                                    |                                         |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                                                                                                               | Description                             |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The listener to set the orientation of. |
| lookat_x |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The x look vector (default 0).          |
| lookat_y |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The y look vector (default 0).          |
| lookat_z |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The z look vector (default -1).         |
| up_x     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The x up vector (default 0).            |
| up_y     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The y up vector (default 1).            |
| up_z     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The z up vector (default 0).            |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _m = camera_get_view_mat(view_camera[0]);
audio_listener_set_position(global.Player_Listener, _m[0], _m[1], _m[2]);
audio_listener_set_orientation(info[? "index"], _m[3], _m[4], _m[5], _m[6], _m[7], _m[8]);
```

The above code retrieves the view matrix for camera view \[0\] and then
uses it to set the audio listener position and orientation for the
listener with the ID stored in the global variable "Player_Listener".
