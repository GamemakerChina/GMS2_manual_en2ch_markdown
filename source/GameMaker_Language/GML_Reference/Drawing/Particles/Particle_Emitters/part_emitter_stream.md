# part_emitter_stream

This function allows you to set an emitter to stream a specific type of
particle and is typically used the create event as it is a one off code
that sets the emitter to generate the number of particles specified
every step of the game there-after. The particles are emitted following
the distribution, shape and position set by the function [
part_emitter_region() ](part_emitter_region) . You can set the
number of particles being streamed to zero and call this function again
to "switch off" the particle streaming, and the function will also
accept negative numbers for the amount, in which case the emitter will
produce particles based on random chance. For example, if you have the
particle number set to -5, there is a 1:5 chance that a particle will be
produced every step. Should you need the particles to appear all at once
rather than every step, you should be using the function [
part_emitter_burst() ](part_emitter_burst) .

#### Syntax:

``` gml
part_emitter_stream(ps, ind, parttype, number);
```

|          |                                                                                                                                         |                                                  |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                                    | Description                                      |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)     | The particle system that the emitter is in.      |
| ind      |  [Particle Emitter ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Emitters/part_emitter_create)  | The index of the emitter to burst from.          |
| parttype |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)           | The index (type) of the particles to be created. |
| number   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                               | The number of particles to create per step.      |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_emitter_stream(global. Sname, p_emit1, p1, 1);
```

The above code will stream 1 particle every step of the game until the
emitter is destroyed or the stream set to 0.
