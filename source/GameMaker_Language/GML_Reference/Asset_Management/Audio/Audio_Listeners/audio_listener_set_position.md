# audio_listener_set_position

With this function you can change the position of a given *listener*
within the 3D audio space. The default listener index is 0, but you can
use the function [ audio_get_listener_info()
](audio_get_listener_info) to get the different indices available
for the target platform. The example image below shows the default
position for the listener in the audio space:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Listener.png)  
As you can see, the default position is (0, 0, 0) but you would normally
use this function to move the listener around with the player object
within your game and so change the way audio created by emitters is
heard by the player, for example, in the image below of a top down game,
the player instance sets the listener which will cause the audio from
the various emitters to "change" as the player moves around the level:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Audio/Audio_Game.png)  

#### Syntax:

``` gml
audio_listener_set_position(index, x, y, z);
```

|          |                                                                                                                                                                                                                    |                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                                                                                                               | Description                                      |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The listener to set the position of (default 0). |
| x        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The x position of the listener (default 0).      |
| y        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The y position of the listener (default 0).      |
| z        |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                          | The z position of the listener (default 0).      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _vmat = camera_get_view_mat(view_camera[0]);
audio_listener_set_position(global.Player_Listener, _vmat[0], _vmat[1], _vmat[2]);
audio_listener_set_orientation(info[? "index"], _vmat[3], _vmat[4], _vmat[5], _vmat[6], _vmat[7], _vmat[8]);
```

The above code retrieves the view matrix for camera view \[0\] and then
uses it to set the audio listener position and orientation for the
listener with the ID stored in the global variable "Player_Listener".
