# physics_fixture_set_restitution

In physics, restitution is defined as "the return of an object or system
to its original state after elastic deformation", but as the fixtures in
the GameMaker are really rigid bodies and cannot be deformed,
restitution is really a way of saying how "bouncy" the fixture is. This
setting will affect how much an object "bounces" when it collides with
other objects and is co-dependent on other forces that act on the
instance like gravity and friction, and is usually a value between 0 and
1 (higher values can be used but may give unpredictable results). Here
is an illustration of how it works:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Physics/physics_fixture_set_restitution_image.png)  

#### Syntax:

``` gml
physics_fixture_set_restitution(fixture, restitution)
```

|             |                                                                                                                     |                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument    | Type                                                                                                                | Description                                              |
| fixture     |  [Physics Fixture ID](../../../../../GameMaker_Language/GML_Reference/Physics/Fixtures/physics_fixture_create)  | The index of the fixture                                 |
| restitution |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                              | The restitution of the fixture (usually between 0 and 1) |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
physics_fixture_set_restitution(fix_Ball, 0.9);
```

The code above will set the restitution of the fixture indexed in
"fix_ball" to 0.9.
