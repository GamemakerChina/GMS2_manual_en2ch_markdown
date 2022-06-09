# instance_position_list

With this function you can check a position for a collision with all
instances of another object. When you use this you are checking a single
point in the room for all instances of an object, and the check will be
done against the bounding box of the instances or against the mask of
the instances if that object has precise collisions checked. You supply
a [DS list](../../Data_Structures/DS_Lists/DS_Lists) too, so the [
id ](Instance_Variables/id) values of any instances that are
colliding with the calling instance will be added to the end of the
given list. You can
[clear](../../Data_Structures/DS_Lists/ds_list_clear) the list
before calling this function so that it only contains results from this
function call. You also have the option to order the list based on the
distance from the position being checked to the origin of the instances
found to be in collision. Note that the function also accepts the
special keyword [** all **](../../../GML_Overview/Instance_Keywords)
, in which case all instances found to be in collision will be listed.
The function returns the number of instances found, or 0 if none are
found.

#### Syntax:

``` gml
instance_position_list(x, y, obj, list, ordered);
```

|          |                                                                                                                                                                                         |                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                   |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The x position to check for instances.                                        |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The y position to check for instances.                                        |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object to check for instances of.                                         |
| list     |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)                                                                              | The DS list to use to store the IDs of colliding instances.                   |
| ordered  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | Whether the list should be ordered by distance ( true ) or not ( false ).     |

#### Returns:

``` gml
 Real

(The number of instances found to be in collision)
```

#### Example:

``` gml
var _list = ds_list_create();
var _num = instance_position_list(mouse_x, mouse_y, all, _list, false);
if _num &amp;gt; 0
{
    for (var i = 0; i &amp;lt; _num; ++i;)
    {
        instance_destroy(_list[| i]);
    }
}
ds_list_destroy(_list);
```

The above code will check for a collision with all instances found at
the mouse position. These will be added to a DS list, which is then
looped through to destroy each of the instances in collision.
