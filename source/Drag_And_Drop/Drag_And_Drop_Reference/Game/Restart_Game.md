#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Game/i_Game_Restart_Game.png) Restart Game

With this action you can restart the game. This is similar to running
the game for the first time and so the [Other - Game Start
Event](../../../The_Asset_Editors/Object_Properties/Other_Events)
will be triggered, as well as the [Other - Game End
Event](../../../The_Asset_Editors/Object_Properties/Other_Events) .
However it should be noted that global variables will not be
re-initialised unless explicitly coded as such - meaning that if you
don't define and set them in the very first room of the game they will
retain their previous values - and that [Data
Structures](../Data_Structures/Data_Structure_Actions) and
[Particles](../Particles/Particle_Actions) will not be freed either
and so that should be done *before* the Restart Game action is called
*or* in the Game End Event. Also note that the game will *not* restart
the moment this action is called, but rather at the end of the script or
event where the action is placed, so if there are any actions placed
after this one, they will still be called and the game restarted at the
end of the block.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Game/a_Game_Restart_Game.png)  

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Game/e_Game_Restart_Game.png)  
The above action block code will check for a gamepad button press and if
one is detected it will restart the game.
