# part_type_gravity

This function will set the gravity that is to affect each particle of
the given type that is created. The gravity strength value is added to
the particle speed every step and is usually a small value like 0.5,
while the direction is the direction of the gravity "pull" and follows
the standard GameMaker directions of 0° being right, 90° being up, 180°
being left and 270° being down.

#### Syntax:

``` gml
part_type_gravity(ind, grav_amount, grav_direction);
```

|                |                                                                                                                                |                                           |
|----------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument       | Type                                                                                                                           | Description                               |
| ind            |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change. |
| grav_amount    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | Strength of the gravity.                  |
| grav_direction |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The direction of the gravity.             |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_shape(global.p1, pt_shape_pixel);
part_type_size(global.p1, 1, 3, 0, 0);
part_type_scale(global.p1, 1, 1);
part_type_colour1(global.p1, c_white);
part_type_alpha2(global.p1, 1, 0);
part_type_speed(global.p1, 2, 4, 0, 0);
part_type_direction(global.p1, 0, 180, 0, 0);
part_type_gravity(global.p1, 0.20, 270);
part_type_orientation(global.p1, 0, 0, 0, 0, 1);
part_type_blend(global.p1, 1);
part_type_life(global.p1, 15, 60);
```

The above code will set various particle values including the gravity
which will add 0.2 to the speed each step with a direction of 270º, so
will pull the particle "down" towards the bottom of the screen.
