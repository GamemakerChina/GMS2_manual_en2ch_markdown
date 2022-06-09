# shader_set_uniform_i\_array

With this function you can set a shader constant to hold an array of
values. You must previously have gotten the "handle" of the constant
using the function [ shader_get_uniform() ](shader_get_uniform) ,
and you will have to have previously initialised the array. **NOTE** :
All uniforms must be set **after** calling the function [ shader_set()
](shader_set) , and before calling [ shader_reset()
](shader_reset) .

#### Syntax:

``` gml
shader_set_uniform_i_array(handle, array);
```

|          |                                                                                                                            |                                                   |
|----------|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                                                                       | Description                                       |
| handle   |  [Shader Uniform Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_uniform)  | The handle of the shader constant to set.         |
| array    |  [Array](../../../../../GameMaker_Language/GML_Overview/Arrays)                                                        | A previously initialised array of integer values. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shader_set(shader_Glass);
col_array[0] = 255;
col_array[2] = 255;
col_array[3] = 64;
col_array[4] = 128;
shader_params = shader_get_uniform(shader_tint, "cColourArray");
shader_set_uniform_i_array(shader_params, col_array);
draw_self();
shader_reset();
```

The above code will get the handle of the shader constant "cColourArray"
then set that constant to the given array.
