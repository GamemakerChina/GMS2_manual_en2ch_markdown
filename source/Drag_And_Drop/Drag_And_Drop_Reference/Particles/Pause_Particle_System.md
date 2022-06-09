#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Pause_Particle_System.png) Pause Particle System

This action will pause the given particle system. You supply the unique
ID value for the system to pause, as returned when you created the
system with the action [Create Particle
System](Create_Particle_System) . A paused particle system will
still draw the particles that have been spawned but they will no longer
update their colour, position or alpha, nor will they complete their
lifespan and disappear until you resume the system. You can choose to
pause or resume the system using the "State" option. Note that this does
*not* pause emitters that are streaming particles, nor will it stop an
emitter bursting particles - emitters will still create particles when
called, but when the system is paused the particles will do nothing and
be drawn exactly where they are created until you reset the paused state
or call [Update Particle System](Update_Particle_System) .

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Pause_Particle_System.png)  

#### Arguments:

|          |                                                 |
|----------|-------------------------------------------------|
| Argument | Description                                     |
| System   | The unique ID value for the system to be paused |
| State    | Whether to pause or resume the particle system  |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Pause_Particle_System.png)  
The above action block code will check a global variable and if it
returns true then the given particle system will be paused otherwise it
will be resumed.
