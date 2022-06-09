# gpu_get_tex_mip_enable_ext

With this function you can get whether mipmapping is switched off,
switched on for everything or switched on only for texture groups
selected in the [Texture Group
Manager](../../../../Settings/Texture_Groups) on a shader sampler.
You supply the index value for the shader sampler (as returned by the
function [ shader_get_sampler_index()
](../../Asset_Management/Shaders/shader_get_sampler_index) , and the
function will return one of the constants listed below.

#### Syntax:

``` gml
gpu_get_tex_mip_enable_ext(sampler_index);
```

|               |                                                                                                                                  |                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument      | Type                                                                                                                             | Description                            |
| sampler_index |  [Shader Sampler Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_sampler_index)  | The index of the shader sampler to get |

#### Returns:

``` gml
 Constant
```

|                  |                                                                                       |
|------------------|---------------------------------------------------------------------------------------|
| Constant         | Description                                                                           |
|  mip_off         | Mipmapping is disabled.                                                               |
|  mip_on          | Mipmapping for all textures is enabled.                                               |
|  mip_markedonly  | Mipmapping is enabled for textures that have it enabled in the Texture Group options. |

#### Example:

``` gml
var _sampleIndex = shader_get_sampler_index(shd_Glass, "s_Background");
var _spriteTex = sprite_get_texture(sprite_index, 0);
shader_set(shd_Glass);
if gpu_get_tex_mip_enable_ext(_sampleIndex) != mip_on
{
    gpu_set_tex_mip_enable_ext(_sampleIndex, mip_on);
}
texture_set_stage(_sampleIndex , _spriteTex);
shader_reset();
```

The above code enables mipmapping for the given shader texture sampler
if it has not already been enabled.
