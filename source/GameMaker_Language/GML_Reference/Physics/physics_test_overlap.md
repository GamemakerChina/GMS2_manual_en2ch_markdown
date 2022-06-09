# physics_test_overlap

This function can be used to check and see if a physical body (ie: the
fixture of an instance) overlaps, or *will* overlap, when rotated and
placed at a given position in the room. the "angle" argument is the
angle of rotation that the calling instance has (or will have) at the
position to be checked, and the "obj" argument can be either a single
instance id, and object index or the
[*keywords*](../../GML_Overview/Instance_Keywords) **all** or
**other** .

#### Syntax:

``` gml
physics_test_overlap(xpos, ypos, angle, obj);
```

|          |                                                                                                                                                                                   |                                              |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                                                                              | Description                                  |
| xpos     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | The x position in the room to check          |
| ypos     |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | The y position in the room to check          |
| angle    |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                               | The angle to check (of the calling instance) |
| obj      |  [Object Asset](../../../../The_Asset_Editors/Objects) or [Instance ID](../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)    | The object to check for                      |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if physics_test_overlap(x+20, y-35, 0, obj_Bomb)
{
    alarm[0] = room_speed;
    ignited = true;
}
```

The above code will check a position for a physics fixture overlap, and
if there is one, it sets a variable and an alarm.
