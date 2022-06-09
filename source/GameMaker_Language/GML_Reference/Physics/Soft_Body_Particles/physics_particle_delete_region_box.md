# physics_particle_delete_region_box

With this function you can delete (remove) all the particles that fall
within the bounds of the defined rectangular area from the physics
simulation in the current room. The function takes the x and y position
for the center of the area to delete as well as the half width and
height of the rectangle (in pixels) which defines the area.

#### Syntax:

``` gml
physics_particle_delete_region_box(x, y, halfWidth, halfHeight)
```

|            |                                                                         |                                                     |
|------------|-------------------------------------------------------------------------|-----------------------------------------------------|
| Argument   | Type                                                                    | Description                                         |
| x          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position of the center of the area to delete. |
| y          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position of the center of the area to delete. |
| halfWidth  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The *half* width of the rectangle.                  |
| halfHeight |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The *half* height of the rectangle.                 |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_particle_delete_region_box(mouse_x, mouse_y, 32, 32);
```

The above code will delete all particles found in a rectangular area
around the mouse position.
