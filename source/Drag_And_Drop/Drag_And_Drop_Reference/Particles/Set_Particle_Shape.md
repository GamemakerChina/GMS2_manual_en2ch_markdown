#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Shape.png) Set Particle Shape

This action can be used to set the built in sprite shape that a particle
should use when drawing. You supply the unique ID value for the type to
set the shape of (as returned when you created the type with the action
[Create Particle Type](Create_Particle_Type) ) and the shape to use.
Particle shapes are simply white sprites that have been created for
GameMaker to use specifically as particles and consist of the following
forms:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/Particle_Types.png)  
**NOTE** : If you use this action then you should **not** use the action
[Set Particle Sprite](Set_Particle_Sprite) as you can only have a
sprite **or** a shape, but not both.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Set_Particle_Shape.png)  

#### Arguments:

|          |                                               |
|----------|-----------------------------------------------|
| Argument | Description                                   |
| Type     | The ID value for the type to set the shape of |
| Shape    | The shape to use for the particle type        |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Set_Particle_Shape.png)  
The above action block code will create a new particle type and assign
its unique ID value to a global variable. It then proceeds to set all
the properties for the particle type.
