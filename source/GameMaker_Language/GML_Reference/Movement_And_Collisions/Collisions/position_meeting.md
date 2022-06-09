# position_meeting

With this function you can check a position for a collision with another
instance or all instances of an object. When you use this you are
checking a single point in the room for an instance or an object. This
check will be done against the bounding box of the instance or against
the mask of the instance if that instance has precise collisions
checked. If you need to get the unique instance
[**id**](../../Asset_Management/Instances/Instance_Variables/id) if
the object being collided with you should use [ instance_position()
](../../Asset_Management/Instances/instance_position) . This
function also accepts the special
[keywords](../../../GML_Overview/Instance_Keywords) **all** and
**other** .

#### Syntax:

``` gml
position_meeting(x, y, obj);
```

|          |                                                                                                                                                                                         |                                                                                              |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                                  |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The x position to check.                                                                     |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The y position to check.                                                                     |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object (or instance id, or the keywords "all" or "other") to check for a collision with. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if mouse_check_button(mb_left)
{
    if !position_meeting(mouse_x, mouse_y, all)
    {
        instance_create_layer(mouse_x, mouse_y, "Walls", obj_Wall);
    }
}
```

The above code checks for the left mouse button, and if it is pressed it
checks the mouse x/y position for a collision with any instance. If
there is none, then an instance of "obj_Wall" is created.
