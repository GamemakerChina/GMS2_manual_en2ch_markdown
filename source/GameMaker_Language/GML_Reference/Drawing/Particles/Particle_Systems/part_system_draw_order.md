# part_system_draw_order

With this function you can set the way in which particles are drawn when
created on the screen. The default system uses an old \> new look (the
function is set to true ), where old particles are drawn at a higher
depth than newer ones and so appear "beneath" them new particles, but by
setting this function to false you can reverse this order and have the
new particles drawn higher and so appear "beneath" the older ones. The
images below illustrate this, with the image on the left being the
default value of true and the image on the right being false :

  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/frontback.gif)  
  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/backfront.gif)  

**NOTE** : When the particles are being drawn with an additive blend
mode, the effect of this function may not always be obvious.

#### Syntax:

``` gml
part_system_draw_order(ind, oldtonew);
```

|          |                                                                                                                                      |                                                                                       |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                                                           |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to change.                                           |
| oldtonew |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                         | Whether old particles should be drawn behind newer ones (true) or vice versa (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
mysystem = part_system_create();
part_system_draw_order(mysystem, true);
```

This will create a new particle system with the index " mysystem ", and
then it sets particles to draw newer particles atop older ones.
