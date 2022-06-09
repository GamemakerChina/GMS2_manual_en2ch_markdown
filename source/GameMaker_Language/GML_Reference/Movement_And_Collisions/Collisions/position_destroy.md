# position_destroy

This function simply destroys all instances that are found to be in
collision with the specified position. Collisions are based on the mask
of the instances, and if any part of the mask over-laps with the target
point it then the function will destroy that instance. Instances
destroyed in this way will trigger their **Destroy** and **Clean Up**
events.

#### Syntax:

``` gml
position_destroy(x, y);
```

|          |                                                                         |                                                           |
|----------|-------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                    | Description                                               |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x coordinate of where to destroy colliding instances. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y coordinate of where to destroy colliding instances. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button_pressed(mb_left)
{
    position_destroy(mouse_x, mouse_y);
}
```

This will destroy all instances that collide with the position of the
mouse cursor when the left mouse button is pressed.
