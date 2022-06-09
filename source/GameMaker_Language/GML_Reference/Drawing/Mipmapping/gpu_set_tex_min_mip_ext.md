# gpu_set_tex_min_mip_ext

With this function you can set the minimum mipmap level which is
currently used for a given shader sampler. You supply the index value
for the shader sampler (as returned by the function [
shader_get_sampler_index()
](../../Asset_Management/Shaders/shader_get_sampler_index) , and
then give a value, where 0 is for full resolution, 1 is for the first
mipmap, 2 for the second etc...

#### Syntax:

``` gml
gpu_set_tex_min_mip_ext(sampler_index, minmip);
```

|               |                                                                                                                                  |                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument      | Type                                                                                                                             | Description                            |
| sampler_index |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The index of the shader sampler to get |
| minmip        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                           | The minimum mipmap level to use        |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _sampleIndex = shader_get_sampler_index(shd_Glass, "s_Background");
var _spriteTex = sprite_get_texture(sprite_index, 0);
shader_set(shd_Glass);
if gpu_get_tex_min_mip_ext(_sampleIndex) != 0
{
    gpu_set_tex_min_mip_ext(_sampleIndex, 0);
}
texture_set_stage(_sampleIndex , _spriteTex);
shader_reset();
```

The above code sets the minimum mipmap level to 0 for the given shader
texture sampler if it has not already been set to 0.
