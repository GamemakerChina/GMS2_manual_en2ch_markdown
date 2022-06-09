# part_system_layer

This function can be used to switch a particle system from its current
layer to a new one. You supply the particle system ID value (as returned
by the function [ part_system_create_layer()
](part_system_create_layer) ) and then the unique layer ID (as
returned by the function [ layer_create()
](../../../Asset_Management/Rooms/General_Layer_Functions/layer_create)
or the name of the layer to use as a string - for example
"instance_layer" - as defined in the room editor), and the system will
be moved to the new layer.

#### Syntax:

``` gml
part_system_layer(ps, layer);
```

|          |                                                                                                                                                                                                                  |                        |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------|
| Argument | Type                                                                                                                                                                                                             | Description            |
| ps       |  [Particle System ID](../../../../../../GameMaker_Language/GML_Reference/Drawing/Particles/Particle_Systems/part_system_create)                                                                              | The particle system ID |
| layer    |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The new layer ID       |

#### Returns:

``` gml
N/A
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
