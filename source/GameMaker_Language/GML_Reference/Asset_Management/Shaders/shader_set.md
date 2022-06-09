# shader_set

With this function you can set the drawing target to the given shader
and all further drawing will be done using that. You can end shader use
with the function [ shader_reset() ](shader_reset) .

#### Syntax:

``` gml
shader_set(shader);
```

|          |                                                                |                                 |
|----------|----------------------------------------------------------------|---------------------------------|
| Argument | Type                                                           | Description                     |
| shader   |  [Shader Asset](../../../../../The_Asset_Editors/Shaders)  | The index of the shader to use. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
shader_set(shader_Glass);
draw_self();
shader_reset();
```

The above code will set a shader to be used for drawing, then draw the
current sprite used for the instance using it.
