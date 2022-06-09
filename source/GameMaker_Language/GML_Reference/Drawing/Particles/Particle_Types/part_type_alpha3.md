# part_type_alpha3

This function can be used to set a three alpha (transparency) value
gradient for each particle created of the given type. The first alpha is
that which all particles will start with, and the second alpha is the
one that will be blended to half way through its lifetime and the third
alpha is the one with which the particle will end with. A smooth
gradient change will occur through the alphas over the particles
lifetime from one to the other.

#### Syntax:

``` gml
part_type_alpha3(ind, alpha1, alpha2, alpha3);
```

|          |                                                                                                                                |                                           |
|----------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                           | Description                               |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change. |
| alpha1   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The starting alpha of the particle.       |
| alpha2   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The halfway point alpha of the particle.  |
| alpha3   |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                      | The ending alpha of the particle.         |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_alpha3( part_Health, 0.5, 1, 0);
```

The above code will make all particles created of the type indexed in
the variable "part_Health" have an alpha blend from 0.5 to 1 to 0 over
their lifetime.
