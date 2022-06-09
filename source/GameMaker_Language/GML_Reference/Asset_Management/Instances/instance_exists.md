# instance_exists

This function can be used in two ways depending on what you wish to
check. You can give it an object_index to check for, in which case this
function will return true if any active instances of the specified
object exist in the current room, or you can also supply it with an
instance id, in which case this function will return true if that
specific instance exists and is active in the current room. Please note
that this function does *not* take into account those instances that
have been deactivated using the [instance
deactivate](Deactivating_Instances/Deactivating_Instances)
functions.

#### Syntax:

``` gml
instance_exists(obj);
```

|          |                                                                                                                                                                                         |                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                           |
| obj      |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id) or [Object Asset](../../../../../The_Asset_Editors/Objects)    | The object or instance to check for the existence of. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !instance_exists(obj_Enemy)
{
    score += 200;
    room_goto(rm_hiscores);
}
```

The above code checks to see if any instances of the object "obj_Enemy"
exist and if not it adds to the variable "score" and changes room.
