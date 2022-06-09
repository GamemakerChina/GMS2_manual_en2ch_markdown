# part_emitter_exists

With this function you can check to see if the given particle emitter
indexed exists in the given system or not. Note that if the variable
being checked is an uninitialised variable (that a particle emitter
would otherwise have its index assigned to) this will throw an error.

#### Syntax:

``` gml
part_emitter_exists(ps, ind);
```

|          |                                                                                                                                         |                                              |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                                    | Description                                  |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)     | The particle system to check for an emitter. |
| ind      |  [Particle Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_create)  | The index of the emitter to search for.      |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if part_emitter_exists(sname, p_emit1)
{
    part_emitter_burst(sname, p_emit1, part_1, 30);
}
```

The above code will check for the emitter indexed in the variable
"permit" and if it exists, it will burst 30 particles from it.
