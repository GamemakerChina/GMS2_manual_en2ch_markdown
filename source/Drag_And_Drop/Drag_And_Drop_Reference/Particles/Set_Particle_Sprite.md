#  ![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/i_Particles_Set_Particle_Sprite.png) Set Particle Sprite

This action can be used to set the sprite that a particle can use when
drawing. You supply the unique ID value for the type to set the sprite
of (as returned when you created the type with the action [Create
Particle Type](Create_Particle_Type) ) and the sprite resource to
use. If the sprite has sub-images, then the particle will animate
through the frames at the speed set in the Image Editor for the sprite.
Also note that if you set a colour value for the particle (using the
[Set Particle Colour](Set_Particle_Colour) action) then this colour
will be blended with the sprite used, much like setting the image blend
on an instance will blend a colour with the instance sprite (use white
for no blending). **NOTE** : If you use this action then you should
**not** use the action [Set Particle Shape](Set_Particle_Shape) as
you can only have a sprite **or** a shape, but not both.

#### Action Syntax:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/a_Particles_Set_Particle_Sprite.png)  

#### Arguments:

|          |                                                |
|----------|------------------------------------------------|
| Argument | Description                                    |
| Type     | The ID value for the type to set the sprite of |
| Sprite   | The sprite to assign to the particle type      |

#### Example:

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/Drag_And_Drop/Reference/Particles/e_Particles_Create_Particle_Type.png)  
The above action block code will create a new particle type and assign
its unique ID value to a global variable. It then proceeds to set all
the properties for the particle type.
