# physics_set_friction

When you bind a fixture to an instance using [ physics_fixture_bind()
](physics_fixture_bind) this returns an "id" for the bound fixture.
You can use this id to set the friction value of the bound fixture,
*not* the "base" fixture, at any time using this function. Note that the
friction is usually set to a value between 0 and 1, but you can use any
non-negative value if required.

#### Syntax:

``` gml
physics_set_friction(fixture, friction)
```

|          |                                                                                                                     |                                 |
|----------|---------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                                | Description                     |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the id of the bound fixture     |
| friction |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | the new friction value to apply |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var fric = physics_get_friction(fix_id); physics_set_friction(fix_id, fric + 0.1);
```

The code above gets the current friction value for the bound physics
properties of the instance and then sets them to a different value.
