# physics_fixture_set_polygon_shape

This function sets a polygon shape for your fixture, but you will need
to use [ physics_fixture_add_point() ](physics_fixture_add_point) to
actually define the shape of this polygon relative to the origin of the
fixture. The polygon is closed when the fixture is bound to an instance.
You should note too that this function *must* be called before defining
any points, and you must also have at least three points defined for
your polygon before binding it to an instance or you will get an error.

#### Syntax:

``` gml
physics_fixture_set_polygon_shape(fixture)
```

|          |                                                                                                                     |                          |
|----------|---------------------------------------------------------------------------------------------------------------------|--------------------------|
| Argument | Type                                                                                                                | Description              |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | the index of the fixture |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_polygon_shape(fix_Ship); physics_fixture_add_point(fix_Ship, 0,0); physics_fixture_add_point(fix_Ship, -40, 100); physics_fixture_add_point(fix_Ship, 40, 100);
```

The code above will apply a polygon shape to the fixture indexed in the
variable "fix_Ship" and then defines three points to create a triangular
shape.
