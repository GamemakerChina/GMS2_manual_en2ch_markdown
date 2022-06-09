# layer_get_shader

This function can be used to check if the given layer has a shader
assigned to it. You supply the layer ID (which you get when you create
the layer using [ layer_create() ](layer_create) ) or the layer name
(as a string - this will have a performance impact), and the function
will return either the shader index of the shader assigned, or -1 if no
shader is assigned.

#### Syntax:

``` gml
layer_get_shader(layer_id)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |

#### Returns:

``` gml
 Shader Asset

or -1 (if no shader is assigned)
```

#### Example:

``` gml
if layer_get_shader(layer) == -1
{
    layer_shader(layer, shd_Sepia);
}
```

The above code will check to see if the layer that the instance running
the code has a shader assigned to it and if it doesn't one is assigned.
