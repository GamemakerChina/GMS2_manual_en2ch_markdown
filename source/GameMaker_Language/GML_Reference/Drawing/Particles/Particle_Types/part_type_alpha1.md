# part_type_alpha1

This function is used to set a particle type to have a single alpha
value (transparency) for the total duration of the lifetime of each
individual particle, and this can be from 0 (transparent) to 1 (opaque).

#### Syntax:

``` gml
part_type_alpha1(ind, alpha1);
```

|          |                                                                                                                                |                                           |
|----------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                           | Description                               |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change. |
| alpha1   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The alpha of the particle.                |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_alpha1(global.Snow_Part, 0.5);
```

The above code will set all particles created of the particle type
indexed in the global variable "Snow_Part" to have an alpha value of 0.5
(semi-transparent).
