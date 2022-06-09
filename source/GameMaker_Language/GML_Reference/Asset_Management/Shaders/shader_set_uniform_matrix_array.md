# shader_set_uniform_matrix_array

With this function you can set a shader constant to hold an array of
matrix values. You must previously have gotten the "handle" of the
constant using the function [ shader_get_uniform()
](shader_get_uniform) , and you will have to have previously
initialised the array as an array of floating point values, where each
successive group of 16 floats is a 4x4 matrix. **NOTE** : All uniforms
must be set **after** calling the function [ shader_set()
](shader_set) , and before calling [ shader_reset()
](shader_reset) .

#### Syntax:

``` gml
shader_set_uniform_matrix_array(handle, array);
```

|          |                                                                                                                            |                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| Argument | Type                                                                                                                       | Description                                              |
| handle   |  [Shader Uniform Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_uniform)  | The handle of the shader constant to set.                |
| array    |  [Array](../../../../../GameMaker_Language/GML_Overview/Arrays)                                                        | A previously initialised array of floating point values. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shader_set(shader_Glass);
shader_params = shader_get_uniform(shader_tint, "cMatrixArray");
shader_set_uniform_matrix_array(shader_params, matrix_array);
draw_self();
shader_reset();
```

The above code will get the handle of the shader constant "cMatrixArray"
then set that constant to the given array.
