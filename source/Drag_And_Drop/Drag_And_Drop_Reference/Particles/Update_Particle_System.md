#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Update_Particle_System.png) Update Particle System

This action will force the given particle system to update the position,
colour, alpha, etc... You supply the unique ID value for the system to
update (as returned when you created the system with the action [Create
Particle System](Create_Particle_System) ), and each time you call
the action the given system will update **one game frame** , meaning
that you can - for example - call this action within a
[Repeat](../Loops/Repeat) loop and make the particle system update
multiple times in a single game frame (useful for when you want a level
to have any effect that requires particles to be present at the very
start, like snow or rain). You can also use this action when the
particle system has been paused using the [Pause Particle
System](Pause_Particle_System) to manually update the particles in
the system.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Update_Particle_System.png)  

#### Arguments:

|          |                                                  |
|----------|--------------------------------------------------|
| Argument | Description                                      |
| System   | The unique ID value for the system to be updated |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Update_Particle_System.png)  
The above action block code will create a loop which will then update
the particle given system 200 times before continuing.
