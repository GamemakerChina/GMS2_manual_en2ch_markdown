#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Gravity.png) Set Particle Gravity

This action will simulate the effect of gravity on all particles of the
given type. You first specify the particle type ID value (which should
be the same as the value used when you created the particle using the
[Create Particle Type](Create_Particle_Type) action) and then you
can set the gravity force and the direction. Force is a *cumulative*
value and will be added on to the speed vector each game frame, so a
gravity of 1 will add one to the speed value each game frame, while the
direction value is simply the direction in which gravity should "pull"
the particle. Note that for both force *and* direction you can use
negative values, and that direction in GameMaker is calculated with 0°
to the right, 90° to the top, 180° to the left and 270° to the bottom.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Set_Particle_Gravity.png)  

#### Arguments:

|           |                                                          |
|-----------|----------------------------------------------------------|
| Argument  | Description                                              |
| Type      | The ID value for the particle type to set the gravity of |
| Force     | The force of the gravity (in pixels per game frame)      |
| Direction | The direction of the gravity "pull"                      |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Create_Particle_Type.png)  
The above action block code will create a new particle type and assign
its unique ID value to a global variable. It then proceeds to set all
the properties for the particle type.
