# physics_particle_delete_region_circle

With this function you can delete (remove) all the particles that fall
within the bounds of the defined circular area from the physics
simulation in the current room. The function takes the x and y position
for the center of the area to delete as well as the radius (in pixels)
which defines the circular area.

#### Syntax:

``` gml
physics_particle_delete_region_circle(x, y, radius)
```

|          |                                                                         |                                                        |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                    | Description                                            |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position of the center of the area to delete.    |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position of the center of the area to delete.    |
| radius   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The radius (in pixels) of the circular area to delete. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_particle_delete_region_circle(mouse_x, mouse_y, 32);
```

The above code will delete all particles found in a circular area around
the mouse position.
