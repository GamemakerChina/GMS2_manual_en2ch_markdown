# gpu_get_cullmode

This function can be used to retrieve the backface culling mode. The
returned value will be one of the following constants (the default value
is cull_noculling ):

|                                                                                                                     |                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
|  [Culling Mode Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/GPU_Control/gpu_get_cullmode)  |                                                |
| Constant                                                                                                            | Description                                    |
|  cull_noculling                                                                                                     | No culling will be done                        |
|  cull_clockwise                                                                                                     | All clockwise triangles will be culled         |
|  cull_counterclockwise                                                                                              | All counter-clockwise triangles will be culled |

#### Syntax:

``` gml
gpu_get_cullmode();
```

#### Returns:

``` gml
 Culling Mode Constant

(see above for constants)
```

#### Example:

``` gml
if gpu_get_cullmode() != cull_clockwise
{
    gpu_set_cullmode(cull_clockwise);
}
```

The above code gets the current cull mode and if it is not
cull_clockwise it is set to that constant.
