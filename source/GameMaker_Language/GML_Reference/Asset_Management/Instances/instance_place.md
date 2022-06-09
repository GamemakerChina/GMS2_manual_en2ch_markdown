# instance_place

With this function you can check a position for a collision with another
instance or all instances of an object using the collision mask of the
instance that runs the code for the check. When you use this you are
effectively asking GameMaker to move the instance to the new position,
check for a collision, move back and tell you if a collision was found
or not. This will work for precise collisions, but only if both the
instance and the object being checked for have precise collision masks
selected otherwise only bounding box collisions are applied. This
function will return the unique instance [ id
](Instance_Variables/id) of the object being collided, but if that
is not needed it is slightly faster to use the function [
place_meeting()
](../../Movement_And_Collisions/Collisions/place_meeting) . This
function also accepts the special keywords **all** and **other** and
will return the [keyword](../../../GML_Overview/Instance_Keywords)
**noone** if no collision occurs, or the unique instance ID value of the
instance found if a collision does occur.

#### Syntax:

``` gml
instance_place(x, y, obj);
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
var _inst = instance_place(x, y, obj_Enemy);
if _inst != noone
{
    hp -= _inst.dmg;
    instance_destroy(_inst);
}
```

The above code will check for a collision with instances of "obj_Enemy"
and if there is one, it will reduce the "hp" variable by the amount
stored in the colliding instance's "dmg" variable and then destroy the
colliding instance.
