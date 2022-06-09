#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/i_Audio_Get_Audio_Pitch.png) Get Audio Pitch

This action will retrieve the pitch of the sound resource you supply.
The return value will be a *multiplier* for the actual recorded pitch of
the sample, where a value of 1 is no change. For more information on
pitch see the action [Set Audio Pitch](Set_Audio_Pitch) .

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/a_Audio_Get_Audio_Pitch.png)  

#### Arguments:

|          |                                                 |
|----------|-------------------------------------------------|
| Argument | Description                                     |
| Sound    | The sound resource to get the pitch of          |
| Target   | The target variable to store the returned pitch |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Audio/e_Audio_Get_Audio_Pitch.png)  
The above action block code first gets the pitch for the given sound and
stores it in a temporary local variable. It then checks for a key press,
and if one is detected, the value of the pitch is checked to see if it
is less than 2. If it is, then the sound is stopped, the pitch variable
has 0.1 added to it, and then this variable is used to set the pitch of
the sound again before it is played.
