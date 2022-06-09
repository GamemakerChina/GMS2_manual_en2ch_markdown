# physics_remove_fixture

This function removes (or "un-binds") a fixture from an instance or
instances. It requires the unique "id" of the bound fixture (as returned
by the function [ physics_fixture_bind() ](physics_fixture_bind) and
it will remove all the currently defined physics properties for the
instance, permitting you to redefine a new fixture and bind that to the
instance. In this way you can change the instances physical properties
without having to destroy and re-create it.

#### Syntax:

``` gml
physics_remove_fixture(id, fixture)
```

|          |                                                                                                                       |                                                               |
|----------|-----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                                                                  | Description                                                   |
| id       |  [Instance ID](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Instances/Instance_Variables/id)  | The ID of the instance to remove the fixture from             |
| fixture  |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)    | The ID of the fixture that is to be removed from the instance |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_remove_fixture(id, my_fix);
```

The code above will remove the fixture with the "id" stored in the
variable "my_fix" from the instance.
