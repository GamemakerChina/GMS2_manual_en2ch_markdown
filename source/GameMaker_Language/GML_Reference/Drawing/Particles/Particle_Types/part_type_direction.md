# part_type_direction

This function is used to determine the direction of the particle when it
is created and can also be used to make the particle increase or
decrease its direction over its lifetime. The minimum and maximum
direction values default at 0, which means that the particle will move
to the right with no variation, but these values can be changed to limit
the direction of movement following the standard GameMaker directions of
0 being right, 90 being up, 180 being left and 270 being down. If you
set them to the same value the particles will only move in one
direction. You can also set an increment value which will add (if a
positive number) or subtract (if a negative number) an amount of degrees
to the direction over its lifetime. This value can be a minimum of (+/-)
0.01. Finally, you can set the "wiggle" factor. This is a value that
will be added or subtracted randomly to the direction each step of the
particles lifetime. Obviously larger values are more pronounced than
smaller ones, and this value can even be a negative with the maximum
range being between -20 and 20.

#### Syntax:

``` gml
part_type_direction(ind, dir_min, dir_max, dir_incr, dir_wiggle);
```

|            |                                                                                                                                |                                                                                         |
|------------|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| Argument   | Type                                                                                                                           | Description                                                                             |
| ind        |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.                                               |
| dir_min    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum direction the particle can start at.                                        |
| dir_max    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum direction the particle can start at.                                        |
| dir_incr   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | How much the particle direction should increase or decrease per step.                   |
| dir_wiggle |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | How much should randomly be added or subtracted from the particle's direction per step. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_shape(particle1, pt_shape_pixel);
part_type_size(particle1, 0.19, 0.79, 0.01, 0);
part_type_scale(particle1, 5, 5);
part_type_colour3(particle1, 32768, 8454016, 8454016);
part_type_alpha3(particle1, 0, 0.80, 0);
part_type_speed(particle1, 8, 10, -0.50, 1);
part_type_direction(particle1, 0, 359, 1, 20);
part_type_gravity(particle1, 0, 270);
part_type_orientation(particle1, 0, 359, 0, 0, 1);
part_type_blend(particle1, 1);
part_type_life(particle1, 10, 50);
```

The above code will set various particle values including the direction
which will be random value between 0 and 359 degrees. It will also go up
by 1 degree each step and has a random amount added to it of anywhere
between 0 and 20 each step too.
