# shader_get_sampler_index

Since you cannot change the value of a shader sampler within the shader
itself, you have to set it before calling the shader using one of the
available **uniform set** functions. However, to be able to do *that*
you must first call this function to get the "handle" of the shader
sampler that you will want to set. NOTE Although a shader is made up of
two discreet programs (vertex and fragment) this function will not
differentiate between the two and will return the handle of the shader
sample from either of them.

#### Syntax:

``` gml
shader_get_sampler_index(shader, uniform);
```

|          |                                                                           |                                                     |
|----------|---------------------------------------------------------------------------|-----------------------------------------------------|
| Argument | Type                                                                      | Description                                         |
| shader   |  [Shader Asset](../../../../../The_Asset_Editors/Shaders)             | The index of the shader to use.                     |
| uniform  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The shader sampler to get the handle of (a string). |

#### Returns:

``` gml
 Shader Sampler Handle
```

#### Example:

``` gml
glassshader_bgsampler = shader_get_sampler_index(GlassShader, "s_BackgroundSampler")
spr = sprite_get_texture(sprite_index, 0);
shader_set(GlassShader);
texture_set_stage(glassshader_bgsampler, spr);
shader_reset();
```

The above code will get the *handle* for the sampler within the shader
indexed as "GlassShader" and then set that shader constant to the given
sprite texture.
