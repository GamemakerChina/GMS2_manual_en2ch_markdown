# instance_position

With this function you can check a position for a collision with another
instance or all instances of an object. When you use this you are
checking a single point in the room for an instance or an object. This
check will be done against the bounding box of the instance or against
the mask of the instance if that instance has precise collisions checked
and will return the unique instance [ id ](Instance_Variables/id) .
If you do not need the id of the colliding instance you should consider
using [ position_meeting()
](../../Movement_And_Collisions/Collisions/position_meeting)
instead. This function also accepts the special
[keywords](../../../GML_Overview/Instance_Keywords) **all** and
**other** and will return the keyword **noone** if no collision occurs
or the unique ID value of the instance found if a collision does occur.

#### Syntax:

``` gml
instance_position( x, y, obj );
```

|          |                                                                                                                                                                                         |                                        |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                            |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The x position to check for instances. |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The y position to check for instances. |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object to check for instances of.  |

#### Returns:

``` gml
 Instance ID

or

 noone
```

#### Example:

``` gml
var inst;
inst = instance_position(mouse_x, mouse_y, obj_Pause_Button);
if (inst != noone)
{
    with (inst) image_index=1;
    instance_create_layer(room_width / 2, 0, "Controllers", obj_Menu);
}
```

The above code will check for a collision with an instance of
"obj_Pause_Button" at the mouse position, and if there is one it will
then use the returned id to set its image_index to a new value before
creating a new instance of the object "obj_Menu".
