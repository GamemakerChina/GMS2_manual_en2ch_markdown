#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Destroy_Particle_Type.png) Destroy Particle Type

This action will "destroy" the given particle type created by the action
[Create Particle Type](Create_Particle_Type) (ie: free up the memory
used by the particle type). This action should be called whenever you no
longer need a particle type in your game, or whenever you wish to
re-create the particle type (for example, just before calling a [Game
Restart](../Game/Restart_Game) ).

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Destroy_Particle_Type.png)  

#### Arguments:

|          |                                      |
|----------|--------------------------------------|
| Argument | Description                          |
| Type     | The ID value for the type to destroy |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Destroy_Particle_System.png)  
The above action block code will check for the "Space" key being pressed
and if it is detected then it removes the particle system and different
particle types defined in the given global variables and then restarts
the game.
