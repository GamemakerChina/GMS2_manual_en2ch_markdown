#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/i_Audio_Set_Audio_Position.png) Set Audio Position

With this action you can set a sound to play at a specific time. You
give the sound to play, and the time to start it from, but this action
will *not* play the sound for you, it will simply set the play position
for the sound. To use this action you must *first* set the position
*then* play the sound using the action [Play Audio](Play_Audio) ,
otherwise you will here no change in position until the next time you
play the same sound resource (which will start at the new position). The
position is set in seconds - you can use decimal values - and you can
get the total sound length using the action [Get Audio
Length](Get_Audio_Length) , although if you provide a value greater
than the length of the desired sound this will be wrapped so if the
sound is 10 seconds long and you give 12 seconds as the start position,
the sound will start at 2 second in.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/a_Audio_Set_Audio_Position.png)  

#### Arguments:

|          |                                                |
|----------|------------------------------------------------|
| Argument | Description                                    |
| Sound    | The sound resource to set the play position of |
| Time     | The time to set (in seconds)                   |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/e_Audio_Get_Audio_Length.png)  
The above action block code gets the playing length of the given sound
resource and stores it in a temporary local variable. This is then used
to generate a random value between 0 and the length of the sound, which
is then stored in a different temporary local variable. This new random
value is then used to set the start position for the sound and the sound
is then played.
