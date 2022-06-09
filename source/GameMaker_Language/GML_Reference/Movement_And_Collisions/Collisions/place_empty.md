# place_empty

You can use this function to check and see if the calling instance would
collide with *any other instance* of an object or all instances in your
game. For this to collision to resolve correctly, the instance running
the code must have a valid collision mask (either for the sprite itself,
or through the [ mask_index
](../../Asset_Management/Sprites/Sprite_Instance_Variables/mask_index)
) and it will only register collisions with those instances that also
have a valid mask. The function is testing if there are no collisions
should the calling instance be placed at a specific position, and you
can supply an optional argument to refine the check to only check if a
position is free of collisions with instances of the given type. Note
that if no optional object ID is supplied, the check will be done
against *all* instances within the room. The collision checking will be
either precise or based on the bounding box of the instance, depending
on what kind of collision mask has been selected, but for precise
collisions to work correctly, all instances in the check should have
precise collision masks. Note that the given x/y coordinates will be
floored to the nearest integer before the check is performed.

#### Syntax:

``` gml
place_empty(x, y, [object_id]);
```

|               |                                                                         |                                         |
|---------------|-------------------------------------------------------------------------|-----------------------------------------|
| Argument      | Type                                                                    | Description                             |
| x             |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The x position to check.                |
| y             |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The y position to check.                |
| \[object_id\] |  [Object Asset](../../../../../The_Asset_Editors/Objects)           |  OPTIONAL The object to check against.  |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if place_empty(mouse_x, mouse_y, obj_Enemy)
{
    x = mouse_x;
    y = mouse_y;
}
```

The above code will check for a collision with any other instance of the
object "obj_Enemy", as if the calling instance were to be placed at the
same position as the mouse. If there is no collision detected, then the
instance has its x/y coordinates set to those of the mouse.
