#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/i_Audio_Stop_Audio.png) Stop Audio

This action can be used to stop a sound from playing. You select the
sound from the asset explorer and all instances of that sound will stop
playing (so if you have set the same sound to play in three different
events then all of them will stop).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/a_Audio_Stop_Audio.png)  

#### Arguments:

|          |                            |
|----------|----------------------------|
| Argument | Description                |
| Sound    | The sound resource to stop |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/e_Audio_Play_Audio.png)  
The above action block code checks for a mouse button press and if one
is detected it then checks a global variable to see if it is not true.
If it is not true, then a sound is played (and looped) and the global
variable set to true , otherwise the sound is stopped and the global
variable is set to false .
