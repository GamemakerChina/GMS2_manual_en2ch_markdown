# layer_shader

With this function you can assign a shader resource to any given layer
and the layer will then be rendered using that shader. You supply either
the unique ID value of the layer or the name of the layer (as a string -
this will have a performance impact) , along with the ID of the shader
to use. The shader must have been created previously in the Asset
Browser and the shader index (the name of the shader resource) is then
passed to this function. If the layer assigned has instances added to
it, then the shader will be applied to *all* the draw events that the
instance uses - for example if the instance has a Draw GUI Begin event,
then the shader will be applied automatically to it. The shader will
also affect any other graphic elements drawn on that layer, like sprite
assets or tile maps. Note that the function is *not* meant to be called
in any draw events or step events, but rather only needs to be called at
the start of the room in the **Room Creation Code** or in the **Create
Event** / **Room Start Event** of an instance.

#### Syntax:

``` gml
layer_shader(layer_id, shader)
```

|          |                                                                                                                                                                                                                  |                                                                            |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                                                                                                                                                             | Description                                                                |
| layer_id |  [String](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Layer ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Rooms/General_Layer_Functions/layer_get_id)    | The unique ID value of the layer to target (or the layer name as a string) |
| shader   |  [Shader Asset](../../../../../../The_Asset_Editors/Shaders)                                                                                                                                                 | The shader index to assign to the layer                                    |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var lay_id = layer_get_id("Instances");
layer_shader(lay_id, shd_Sepia);
```

The above code will assign the shader resource "shd_Sepia" to the given
layer for all drawing.
