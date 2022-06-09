# collision_ellipse_list

This function is the same as the [ collision_ellipse()
](collision_ellipse) function, only instead of just detecting one
instance in collision at a time, it will detect multiple instances. You
supply the x/y positions of the top left and bottom right of the
elliptical area to check along with the object to check for, and you can
set the check to be precise (in which case all instances being checked
will need to have *precise* collision masks) and whether the check
should include the calling instance or not. You supply a [DS
list](../../Data_Structures/DS_Lists/DS_Lists) too, so the [ id
](../../Asset_Management/Instances/Instance_Variables/id) values of
any instances that are colliding with the calling instance will be added
to the end of the given list. You can
[clear](../../Data_Structures/DS_Lists/ds_list_clear) the list
before calling this function so that it only contains results from this
function call. You also have the option to order the instances based on
their distances from the origin of the elliptic area to their origins.
The function returns the number of instances found, or 0 if none are
found. Note that instead of an object index you can supply the [instance
keyword](../../../GML_Overview/Instance_Keywords) all , to check for
all instances in the current room, which may include the instance
running the code (depending on the notme argument).

#### Syntax:

``` gml
collision_ellipse_list(x1, y1, x2, y2, obj, prec, notme, list, ordered);
```

|          |                                                                                                                                                                                         |                                                                                                                                  |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                    | Description                                                                                                                      |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The x coordinate of the left side of the ellipse to check.                                                                       |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The y coordinate of the top side of the ellipse to check.                                                                        |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The x coordinate of the right side of the ellipse to check.                                                                      |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                  | The y coordinate of the bottom side of the ellipse to check.                                                                     |
| obj      |  [Object Asset](../../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object to check for instance collisions.                                                                                     |
| prec     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | Whether the check is based on precise collisions ( true , which is slower) or its bounding box in general ( false , faster).     |
| notme    |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | Whether the calling instance, if relevant, should be excluded ( true ) or not ( false ).                                         |
| list     |  [DS List ID](../../../../../GameMaker_Language/GML_Reference/Data_Structures/DS_Lists/ds_list_create)                                                                              | The DS list to use to store the IDs of colliding instances.                                                                      |
| ordered  |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | Whether the list should be ordered by distance ( true ) or not ( false ).                                                        |

#### Returns:

``` gml
 Real

(The number of instances found to be in collision)
```

#### Example:

``` gml
var _list = ds_list_create();
var _num = collision_ellipse_list(x - 100, y - 100, x + 100, y + 100, obj_Enemy, false, true, _list, false);
if _num &amp;gt; 0
{
    for (var i = 0; i &amp;lt; _num; ++i;)
    {
        instance_destroy(_list[| i]);
    }
}
ds_list_destroy(_list);
```

The code above will check an elliptical area 100 pixels around the
calling instance position for collisions with instances of "obj_Enemy".
If there are any collisions, then the pre-created list is looped through
and each instance that was in the collision is destroyed.
