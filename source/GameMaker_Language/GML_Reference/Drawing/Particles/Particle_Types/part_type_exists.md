# part_type_exists

With this function you can check to see if the given particle type
indexed exists in the game or not. Note that if the variable being
checked is an uninitialised variable (that a particle type would
otherwise have its index assigned to) this will throw an error.

#### Syntax:

``` gml
part_type_exists(ind);
```

|          |                                                                                                                                |                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                           | Description                                  |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !part_type_exists(global.p1)
{
    global.p1 = part_type_create();
}
```

The above code checks to see if the global variable "p1" stores the
index of a particle type and if it does not it creates one.
