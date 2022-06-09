# part_type_clear

With this function you can "reset" a particle, returning all the values
for each of the functions relating to the particle (life, colour, alpha,
orientation etc...) to their default values. Note that this function
does not remove any particles currently visible in the room from the
screen, for that you should be using [ part_particles_clear()
](../Particle_Systems/part_particles_clear) .

#### Syntax:

``` gml
part_type_clear(ind);
```

|          |                                                                                                                                |                                          |
|----------|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                                           | Description                              |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_clear(global.explode_part);
```

The above code will clear the particle type indexed in the global
variable "explode_part" to its default values.
