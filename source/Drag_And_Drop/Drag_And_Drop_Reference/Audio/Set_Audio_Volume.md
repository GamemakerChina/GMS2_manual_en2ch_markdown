#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/i_Audio_Set_Audio_Volume.png) Set Audio Volume

With this action you can set the volume of a given sound. You select the
sound from the asset explorer and then set the volume value. The volume
can be between 0 (silent) and 1 (full volume) and the scale is linear,
such that a value of 0.5 would be half volume. Note that this action
will affect all instances of the sound that are playing currently in the
room, and will affect all future instances of the sound played.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/a_Audio_Set_Audio_Volume.png)  

#### Arguments:

|          |                                                       |
|----------|-------------------------------------------------------|
| Argument | Description                                           |
| Sound    | The sound resource to set the volume of               |
| Volume   | The new volume for the sound (from 0 to 1, default 1) |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/e_Audio_Get_Audio_Volume.png)  
The above action block code checks a global variable to see if it is
true or false. If it is true then the volume of the given sound is
retrieved and stored in a temporary local variable. The value is then
checked to see if it is not equal to 0.5, and if it is not, then the
volume of the sound is set to 0.5. If the global variable evaluates to
false , then the sound has its volume set to 1.
