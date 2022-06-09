# part_type_life

This is the function that governs how long each individual particle of
the indicated type remains on the screen. As with other particle
functions, you provide a minimum and a maximum value (in steps)and each
particle lifespan will be a random number of steps from within the
specified range. To have all particles with the same lifetime, set the
two values to be the same.

#### Syntax:

``` gml
part_type_life(ind, life_min, life_max);
```

|          |                                                                                                                                |                                           |
|----------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                           | Description                               |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change. |
| life_min |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The minimum lifespan of the particles.    |
| life_max |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The maximum lifespan of the particles.    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_life(part_Flare, room_speed, room_speed * 2);
```

The above code will set all particles created of the particle type
indexed in the variable "part_Flare" to have a lifetime of between 1 and
2 seconds, based on the current room-speed.
