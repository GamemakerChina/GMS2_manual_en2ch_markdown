# physics_fixture_set_box_shape

This function defines a box shape for your fixture. It takes the *half*
width and height as the physics world uses this value far more than
whole width/height values to determine things like collisions.

#### Syntax:

``` gml
physics_fixture_set_box_shape(fixture, halfWidth, halfHeight)
```

|            |                                                                                                                     |                              |
|------------|---------------------------------------------------------------------------------------------------------------------|------------------------------|
| Argument   | Type                                                                                                                | Description                  |
| fixture    |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture     |
| halfWidth  |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | the *half* width of the box  |
| halfHeight |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | the *half* height of the box |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_box_shape(fix_Border, room_width/2, 10);
```

The code above will apply a box shape to the fixture indexed in the
variable "fix_Border" with a width of the room and a height of 20
pixels.
