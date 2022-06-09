# physics_fixture_set_friction

Friction is the force that resists the relative motion of material
elements sliding against each other, which in the GameMaker physics
world, translates as the loss of momentum caused by the collision of two
instances with fixtures bound to them. So, when two instances collide,
their motion is affected by this value, with a high friction causing a
larger loss of momentum than a lower value. Note that the friction is
usually set to a value between 0 and 1, but you can use any non-negative
value if required.

#### Syntax:

``` gml
physics_fixture_set_friction(fixture, friction)
```

|          |                                                                                                                     |                             |
|----------|---------------------------------------------------------------------------------------------------------------------|-----------------------------|
| Argument | Type                                                                                                                | Description                 |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture    |
| friction |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | the friction of the fixture |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_friction(fix_Brick, 0.1);
```

The code above will set the friction of the fixture indexed in
"fix_brick" to 0.1.
