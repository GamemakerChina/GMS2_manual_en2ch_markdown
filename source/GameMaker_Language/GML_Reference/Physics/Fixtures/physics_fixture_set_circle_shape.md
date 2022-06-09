# physics_fixture_set_circle_shape

This function defines a circle shape for your fixture with a radius
defined by the argument "rad".

#### Syntax:

``` gml
physics_fixture_set_circle_shape(fixture, rad)
```

|          |                                                                                                                     |                          |
|----------|---------------------------------------------------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                                                                | Description              |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture |
| rad      |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | radius of the circle     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_circle_shape(fix_Ball, sprite_get_width(spr_Ball) / 2);
```

The code above will apply a circle shape to the fixture indexed in the
variable "fix_Ball" with a radius the same as that of the width of the
sprite "spr_Ball" divided by 2.
