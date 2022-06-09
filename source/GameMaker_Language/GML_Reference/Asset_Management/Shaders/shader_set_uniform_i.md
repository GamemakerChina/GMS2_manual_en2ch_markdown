# shader_set_uniform_i

With this function you can set the value (or values) of a shader
constant. You must previously have gotten the "handle" of the constant
using the function [ shader_get_uniform() ](shader_get_uniform) ,
and you will have to know what type of constant it is to pass the
correct number of integer values through to it, ie: if you have a vec2
you will need to pass two values to the function. **NOTE** : All
uniforms must be set **after** calling the function [ shader_set()
](shader_set) , and before calling [ shader_reset()
](shader_reset) .

#### Syntax:

``` gml
shader_set_uniform_i(handle, value1 [, value2, value3, value4]);
```

|                   |                                                                                                                            |                                                              |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument          | Type                                                                                                                       | Description                                                  |
| handle            |  [Shader Uniform Handle](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Shaders/shader_get_uniform)  | The handle of the shader constant to set.                    |
| value1 ... value4 |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                     | The integer value (or values) to set the shader constant to. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shader_set(shader_Glass);
shader_params = shader_get_uniform(shader_glass, "u_vParams");
shader_set_uniform_i(shader_params, 0, 65, 255);
draw_self();
shader_reset();
```

The above code will get the handle of the shader constant "u_vParams" (
a vec3 ), then set that constant to the given integer values.
