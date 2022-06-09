# physics_fixture_create

The first step in setting up a fixture is creating it with this
function. The returning index should be stored in a variable to be used
in all further functions that are used to define and use this fixture.

#### Syntax:

``` gml
physics_fixture_create()
```

#### Returns:

``` gml
 Physics Fixture ID
```

#### Example:

``` gml
fix_Ball = physics_fixture_create();
```

The code above will create a fixture and store its index in the variable
"fix_Ball".
