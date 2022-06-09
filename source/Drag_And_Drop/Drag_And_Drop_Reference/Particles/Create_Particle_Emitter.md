#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Create_Particle_Emitter.png) Create Particle Emitter

To be able to see your particles you need to have first created a
[Particle System](Create_Particle_System) , then have defined some
[particle types](Create_Particle_Type) and then finally created a
**particle emitter** using this action. To create the emitter, you call
this action and assign the emitter to a particle system that you have
previously created (see [Particle System](Create_Particle_System) )
and then give a target variable to store it's unique ID value for use in
further actions. You can choose to flag this variable as being a
temporary local variable, but that will mean that it is discarded at the
end of the action script or event, meaning that the emitter will still
exist but leave you without any means to access it, so care must be
taken when using this (in general emitters will never need to be stored
in a temporary local variable, but for certain things, like drawing
particles to a surface, it may be required). **IMPORTANT!** If your
particle system is **persistent** then you must either destroy all
emitters at the end of each room using [Destroy Particle
Emitter](Destroy_Particle_Emitter) and re-create them again in the
next room as required, or store their ID values in **global** variables
so that they can be accessed anytime in any room, or have them created
by a persistent object, so that the object will persist and be able to
access them through instance variables. Also note that if you call the
[Restart Game](../Game/Restart_Game) action you should destroy the
particle system beforehand so that the system and the emitters assigned
are removed from memory before starting again. Failure to properly
remove emitters from system memory as outlined above will lead to a
**memory leak** . This happens when a resource is added to memory and
then "de-referenced", meaning that GameMaker has no way to interact with
that resource any more. This leads to the memory being clogged by
inaccessible resources which in turn can cause issues with your game.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Create_Particle_Emitter.png)  

#### Arguments:

|          |                                               |
|----------|-----------------------------------------------|
| Argument | Description                                   |
| System   | The ID value for the global emitter to create |
| Target   | The target variable to hold the emitter ID    |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Create_Particle_Emitter.png)  
The above action block code will create a particle emitter, set it's
region, and then set it to emit a stream of particles.
