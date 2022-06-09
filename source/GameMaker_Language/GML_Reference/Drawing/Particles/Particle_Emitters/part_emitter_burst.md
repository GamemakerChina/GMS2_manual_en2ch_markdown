# part_emitter_burst

This function allows you to set an emitter to burst a specific type of
particle and is typically used in alarms and destroy events as it is a
one off code that creates the number of particles specified all at once
following the distribution, shape and position set by the function [
part_emitter_region() ](part_emitter_region) . Should you need the
particles to appear every step, you should be using the function [
part_emitter_stream() ](part_emitter_stream) rather than calling
this function every step.

#### Syntax:

``` gml
part_emitter_burst(ps, ind, parttype, number);
```

|          |                                                                                                                                         |                                                  |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                                    | Description                                      |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)     | The particle system that the emitter is in.      |
| ind      |  [Particle Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_create)  | The index of the emitter to burst from.          |
| parttype |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)           | The index (type) of the particles to be created. |
| number   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The number of particles to create.               |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_emitter_burst(global. Sname, p_emit1, p1, 30 + irandom(30));
```

The above code will burst a random number of particles between 30 and 60
from the chosen emitter.
