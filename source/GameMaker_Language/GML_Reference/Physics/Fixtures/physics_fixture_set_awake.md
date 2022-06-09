# physics_fixture_set_awake

When you start a room with physics, or bind fixtures to instances, the
fixtures are always considered to be "awake"... that is to say, they are
processing events and interacting with the surrounding instances.
However this can sometimes lead to problems, especially if you have a
number of instances with fixtures that are side by side when a room
starts (think of a tower made of various instances with fixtures) as
with them being "awake" they will move and possibly change position due
to the sudden start of gravity and collisions affecting them. In these
cases you can use this function to flag the fixture as been "asleep", in
which case it will not be processing anything when it is first created
in the room.

#### Syntax:

``` gml
physics_fixture_set_awake(fixture, state)
```

|          |                                                                                                                     |                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument | Type                                                                                                                | Description                                              |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture                                 |
| flag     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | whether a fixture is awake ( true ) or not ( false )     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_awake(fix_Cloud, true);
```

The code above flag the fixture as being "awake" when bound to an
instance.
