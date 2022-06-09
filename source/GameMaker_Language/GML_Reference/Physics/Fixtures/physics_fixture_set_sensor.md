# physics_fixture_set_sensor

Some times you will want your game to detect and recognise when two
instances with fixtures collide, but not have any physical reaction to
the collision. This can be done by converting the fixture into a sensor,
which basically means that they will generate a collision event but with
no physical response so that you can use these instances as "triggers"
for other events to happen in the game room. Any fixture can be flagged
as a sensor, and it makes no difference if the instance it is bound to
is static or in movement. **NOTE** : A sensor fixture will fire off the
collision event when the collision **first occurs only** , meaning you
don't get a stream of collision events as the two bodies continue to
overlap (which is what would traditionally occur). If they stop
overlapping and overlap subsequently there will be another collision
event triggered.

#### Syntax:

``` gml
physics_fixture_set_sensor(fixture, state)
```

|          |                                                                                                                     |                                                     |
|----------|---------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                                | Description                                         |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture                            |
| state    |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                           | whether a fixture is a sensor (true) or not (false) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_sensor(fix_Cloud, 1);
```

The code above will turn the sensor state of the fixture indexed in
"fix_Cloud" to true.
