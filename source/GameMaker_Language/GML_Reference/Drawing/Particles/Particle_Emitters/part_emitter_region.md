# part_emitter_region

This function is used to set their position of a particle emitter within
the current room. You specify the bounding box of the area within the
function and then use any of a series of constants to define the final
emitter shape within this bounding box as well as the distribution of
particles within the shape. The available constants for distribution
shapes are listed below:

|                                                                                                                                                     |                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
|  [Particle Emitter Shape Constant](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_region)  |                                                                                                     |
| Constant                                                                                                                                            | Description                                                                                         |
|  ps_shape_rectangle                                                                                                                                 | A rectangular shape that fills the given area.                                                      |
|  ps_shape_ellipse                                                                                                                                   | An ellipse, with the width and height defined by the area.                                          |
|  ps_shape_diamond                                                                                                                                   | A diamond shape with the points at half width and half height.                                      |
|  ps_shape_line                                                                                                                                      | A single line, where the start point is the left and top and the end point is the right and bottom. |

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/Emitter_Shapes.png)  
Apart from the distribution shapes, you can also define the distribution
curve for the particles that are to be emitted. The available constants
for distribution curves are listed below:

|                                                                                                                                                            |                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
|  [Particle Emitter Distribution Constant](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_region)  |                                                                                                   |
| Constant                                                                                                                                                   | Description                                                                                       |
|  ps_distr_linear                                                                                                                                           | A Linear distribution where all particles have an equal chance of appearing anywhere in the area. |
|  ps_distr_gaussian                                                                                                                                         | A gaussian distribution where more particles are generated in the center rather than the edges.   |
|  ps_distr_invgaussian                                                                                                                                      | An inverse gaussian distribution where more particles are generated at the edges than center.     |

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/Emitter_Distribution.png)  
**NOTE** : If you need the emitter to move with an instance, you will
have to use this function in the step event and update the emitter
position that way. It is also worth noting that for point emissions
where you do not need to create particles over an area or with a
specific distribution, it is often easier to use [
part_particles_create() ](../Particle_Systems/part_particles_create)
.

#### Syntax:

``` gml
part_emitter_region(ps, ind, xmin, xmax, ymin, ymax, shape, distribution);
```

|              |                                                                                                                                                            |                                                  |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument     | Type                                                                                                                                                       | Description                                      |
| ps           |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)                        | The particle system that the emitter is in.      |
| ind          |  [Particle Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_create)                     | The index of the emitter to set.                 |
| xmin         |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                  | The x coordinate of the left side of the region. |
| xmax         |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                  | The x coordinate of the right side.              |
| ymin         |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                  | The y coordinate of the top of the region.       |
| ymax         |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                  | The y coordinate of the bottom of the region.    |
| shape        |  [Particle Emitter Shape Constant](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_region)         | The shape of the region.                         |
| distribution |  [Particle Emitter Distribution Constant](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_region)  | The distribution style of the particles.         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_emitter_region(global.Sname , emit_1, x - 50, x + 50, y - 50, y + 50, ps_shape_ellipse, ps_distr_linear);
```

The above code will set an emitter to the a 100px tall and 100px wide
elliptical shape around the current (x,y) position of the instance
running the code.
