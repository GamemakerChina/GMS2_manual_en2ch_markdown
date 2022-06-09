# physics_set_density

When you bind a fixture to an instance using [ physics_fixture_bind()
](physics_fixture_bind) this returns an "id" for the bound fixture.
You can use this id to set the density value of the bound fixture, *not*
the "base" fixture, at any time using this function.

#### Syntax:

``` gml
physics_set_density(fixture, density)
```

|          |                                                                                                                     |                                |
|----------|---------------------------------------------------------------------------------------------------------------------|--------------------------------|
| Argument | Type                                                                                                                | Description                    |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the id of the bound fixture    |
| density  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | the new density value to apply |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var density = physics_get_density(fix_id); physics_set_density(fix_id, density - 0.1);
```

The code above gets the current density value for the bound physics
properties of the instance and then sets them to a different value.
