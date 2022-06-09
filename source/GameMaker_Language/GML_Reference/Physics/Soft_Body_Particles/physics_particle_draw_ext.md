# physics_particle_draw_ext

This function will draw a sprite at the position of all the particles
that share the same user defined category value, and that have flags
which coincide with those set for the mask. The mask value is defined in
the same way as you would define the flags when creating the particles
(see the functions [ physics_particle_create()
](physics_particle_create) for an example), ie: using the [bitwise
*or*](../../../../Additional_Information/Bitwise_Operators) "\|" to
mask off the appropriate bits for each flag. **NOTE** : This function
will draw **all** particles in the physics simulation with flags that
coincide with those of the mask, whether they are individual particles
or groups, if the user category is the same. The drawn particle will
ignore the colour and alpha values set when you created it, and will
instead be drawn using the scale, angle, colour and alpha parameters
given in this function. Note that this is purely for drawing a sprite at
the particle position and in no way affects the behaviour of the
particle.

#### Syntax:

``` gml
physics_particle_draw_ext(typemask, category, sprite, subimg, xscale, yscale, ang, col, alpha)
```

|          |                                                                                                                                                 |                                                                   |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| Argument | Type                                                                                                                                            | Description                                                       |
| typemask |  [Physics Particle Flag Constant](../../../../../GameMaker_Language/GML_Reference/Physics/Soft_Body_Particles/physics_particle_create) (s)  | The mask to compare the particles flags with.                     |
| category |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The user defined category to draw (use 0 to draw all categories). |
| sprite   |  [Sprite Asset](../../../../../The_Asset_Editors/Sprites)                                                                                   | The sprite to use for each particle.                              |
| subimg   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The image_index of the sprite to draw.                            |
| xscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The scale factor to apply to the sprite along the x axis.         |
| yscale   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The scale factor to apply to the sprite along the y axis.         |
| ang      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The angle (in degrees) to draw the sprite at.                     |
| col      |  [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)                                        | The colour to blend with the sprite (default is c_white ).        |
| alpha    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The alpha value to use when drawing (0 - 1).                      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var flags = phy_particle_flag_water | phy_particle_flag_viscous | phy_particle_flag_tensile;
physics_particle_draw_ext(flags, 2, sprBlob, 0, 2, 2, 0, c_white, 0.5);
```

The above code will draw a sprite for all the particles in the user
defined category "2" which have the same flags as the given mask, scaled
by 2 along both axis and with an alpha of 0.5.
