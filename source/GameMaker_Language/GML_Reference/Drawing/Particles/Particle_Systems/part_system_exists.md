# part_system_exists

With this function you can check to see if the given particle system
indexed exists in the game or not. Note that if the variable being
checked is an uninitialised variable (that a particle system would
otherwise have its index assigned to) this will throw an error.

#### Syntax:

``` gml
part_system_exists(ind);
```

|          |                                                                                                                                      |                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                    |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The index of the particle system to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !part_system_exists(global.Sname)
{
    global.Sname = part_system_create();
}
```

The above code checks to see if the particle system referenced in the
global variable exists and if it does not it is created.
