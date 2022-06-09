# part_system_get_layer

This function can be used to retrieve the unique layer ID value for the
given particle system. You supply the particle system ID value (as
returned by the function [ part_system_create_layer()
](part_system_create_layer) ) and the function will return the ID
value of the layer.

#### Syntax:

``` gml
part_system_get_layer(ind);
```

|          |                                                                                                                                      |                                                     |
|----------|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                                                                                 | Description                                         |
| ind      |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)  | The particle system ID value to get the layer ID of |

#### Returns:

``` gml
 Layer ID

or 0 (if the layer is an internally managed one)
```

#### Example:

``` gml
if (part_system_get_layer(global.p_sys) != "effects_layer")
{
    part_system_layer(global.p_sys, "effects_layer";
}
```

The above code will check a particle system to see what layer it is on
and if it is not on the given layer it will be changed.
