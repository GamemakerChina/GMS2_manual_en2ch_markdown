#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/i_Audio_Play_Audio.png) Play Audio

This action will set the given sound playing. You select the sound from
the Asset Explorer and then set whether you would like the sound to be
looped or not (a looped sound will play again and again until stopped)
by setting the "Loop" flag.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/a_Audio_Play_Audio.png)  

#### Arguments:

|          |                                                   |
|----------|---------------------------------------------------|
| Argument | Description                                       |
| Sound    | The sound resource to play                        |
| Loop     | Whether to loop the sound or not (off by default) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/e_Audio_Play_Audio.png)  
The above action block code checks for a mouse button press and if one
is detected it then checks a global variable to see if it is not true.
If it is not true, then a sound is played (and looped) and the global
variable set to true , otherwise the sound is stopped and the global
variable is set to false .
