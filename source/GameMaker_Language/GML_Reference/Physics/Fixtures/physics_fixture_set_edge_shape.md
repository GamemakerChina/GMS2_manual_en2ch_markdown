# physics_fixture_set_edge_shape

This function defines an "edge" fixture shape. An edge shape is simply a
line that will generate a collision when other fixtures over lap it, and
can be very useful for generating (for example) terrain, or for creating
borders around a room. The position of the edge is defined using *local*
space, ie: the x/y position of the instance is considered (0,0), so this
should be taken into consideration when creating them (in the code
example below, the instance would have been placed at (0,0) in the room
to avoid complications).

#### Syntax:

``` gml
physics_fixture_set_edge_shape(fixture, local_x1, local_y1, local_x2, local_y2)
```

|          |                                                                                                                     |                               |
|----------|---------------------------------------------------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                                                                | Description                   |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture      |
| local_x1 |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | start x position for the edge |
| local_y1 |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | start y position for the edge |
| local_x2 |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | end x position for the edge   |
| local_y2 |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | end y position for the edge   |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var xx = 0;
var y1 = room_height - 100;
var y2 = room_height - 50 - irandom(100);
for (var i = 0; i &amp;lt; 10; i++;)
{
    var fix = physics_fixture_create();
    physics_fixture_set_edge_shape(fix, xx, y1, xx + 50, y2);
    physics_fixture_bind(fix, id);
    physics_fixture_delete(fix);
    xx += 50;
    y1 = y2;
    y2 = room_height - 50 - irandom(100);
}
```

The above code will create a line of "edge" fixtures with a variety of
heights over the length of the room.
