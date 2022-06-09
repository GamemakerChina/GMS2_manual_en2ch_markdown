# physics_fixture_set_chain_shape

This function defines a "chain" fixture shape. A chain fixture is
comprised of a number of points, which are then connected together using
edge shapes to join them. The function itself takes the index (ID) of
the fixture and can tell the fixture to loop or not. Setting this to
true will connect the last point to the first point with an edge, while
setting it to false will not. Note that this function on prepares the
fixture to accept the points required to make the chain, and these
should be added after calling this function using [
physics_fixture_add_point() ](physics_fixture_add_point) , much as
you would when building a polygon fixture. When creating a chain
fixture, you must give it at least two points but you are not limited in
the number of subsequent points that you can add to make up the finished
fixture.

#### Syntax:

``` gml
physics_fixture_set_chain_shape(fixture, loop)
```

|          |                                                                                                                     |                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument | Type                                                                                                                | Description                                               |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | The index of the fixture                                  |
| loop     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | Whether to close the chain ( true ) or not ( false ).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var xx = -100;
var yy = room_height / 2;
var fix = physics_fixture_create(); physics_fixture_set_chain_shape(fix, false);
for (var i = 0; i &amp;lt; 10; i++;)
{
    physics_fixture_add_point(fix, xx, yy);
    xx += 50 + random(150);
    yy = (room_height / 2) - 250 + irandom(500);
}
physics_fixture_bind(fix, id);
```

The above code will create a line of "edge" fixtures with a variety of
heights over the length of the room.
