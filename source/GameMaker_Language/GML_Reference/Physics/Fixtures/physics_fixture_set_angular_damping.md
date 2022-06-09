# physics_fixture_set_angular_damping

If you think about any rotating object in the "real world", unless it
has a motor or is in space, it slows down over time due to the influence
of external forces (like friction with the air around it). We can use
the function physics_fixture_set_angular_damping() in GameMaker to
simulate this effect and reduce the velocity of rotation of instances in
the physics world, as, without it, any rotating instance would continue
to rotate infinitely. Damping parameters should be between 0 and
infinity, with 0 meaning no damping, and infinity meaning full damping.
Normally you will use a damping value between 0 and 1, but you can use
any non-negative value if required.

#### Syntax:

``` gml
physics_fixture_set_angular_damping(fixture, damping)
```

|          |                                                                                                                     |                                                             |
|----------|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                                                                | Description                                                 |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture                                    |
| damping  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | the angular damping of the fixture, usually between 0 and 1 |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_angular_damping(fix_Ball, 0.1);
```

The code above will set the angular damping of the fixture indexed in
"fix_ball" to 0.1.
