# part_type_blend

With this function you can make your particles be drawn with an additive
blend mode ( true ) or not ( false ). Additive blending is a special
blend mode that adds the luminosity values of each particle as they
overlap, so that light colours will gradually get brighter (until they
appear white) as they overlap, and dark colours become more and more
transparent with black being almost invisible. This function can give
some beautiful particle effects but may not always be necessary. For
example, a smoke trail would have additive blending off to keep the
effect gray, but a flame effect would probably have it on to make the
particles more translucent and brighter.

#### Syntax:

``` gml
part_type_blend(ind, additive);
```

|          |                                                                                                                                |                                                                                |
|----------|--------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Argument | Type                                                                                                                           | Description                                                                    |
| ind      |  [Particle Type ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Types/part_type_create)  | The index of the particle type to change.                                      |
| additive |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                   | Whether the particles should be blended additively (true) or normally (false). |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
part_type_blend(part_Fire, true);
```

The above code will set all particles created of the particle type
indexed in the variable "part_Fire" to have an additive blend mode.
