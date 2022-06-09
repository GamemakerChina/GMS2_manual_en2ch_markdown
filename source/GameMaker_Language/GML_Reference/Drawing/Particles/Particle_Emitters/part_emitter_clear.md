# part_emitter_clear

With this function you can clear the given emitter from the specified
particle system back to its default state. This will also stop any
particles that are being streamed from the emitter at the time, and if
you wish to use the emitter again you will need to set the region
position and particle type using the [ part_emitter_region()
](part_emitter_region) function.

#### Syntax:

``` gml
part_emitter_clear(ps, ind);
```

|          |                                                                                                                                         |                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                                                                                    | Description                                 |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)     | The particle system that the emitter is in. |
| ind      |  [Particle Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_create)  | The index of the emitter to clear.          |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_emitter_clear(Sname, p_emit1 );
```

The above code will clear the particle emitter indexed in the variable
"p_emit1".
