# shader_set_uniform_matrix

With this function you can set the value (or values) of a shader
constant to the current transform matrix (as set using the [Matrix
Functions](../../Maths_And_Numbers/Matrix_Functions/Matrix_Functions)
). You must previously have gotten the "handle" of the constant using
the function [ shader_get_uniform() ](shader_get_uniform) . **NOTE**
: All uniforms must be set **after** calling the function [ shader_set()
](shader_set) , and before calling [ shader_reset()
](shader_reset) .

#### Syntax:

``` gml
shader_set_uniform_matrix(handle);
```

|          |                                                                                                                            |                                           |
|----------|----------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                       | Description                               |
| handle   |  [Shader Uniform Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_uniform)  | The handle of the shader constant to set. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shader_set(shader_Glass);
shader_matrix = shader_get_uniform(shader_glass, "u_vMatrix");
shader_set_uniform_matrix(shader_matrix);
draw_self();
shader_reset();
```

The above code will get the handle of the shader constant "u_vMatrix"
then set that constant to the current transform matrix.
