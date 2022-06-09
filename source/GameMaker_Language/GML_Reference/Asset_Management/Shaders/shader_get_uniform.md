# shader_get_uniform

Since you cannot change the value of a shader constant within the shader
itself, you have to set it before calling the shader using one of the
available **uniform set** functions. However, to be able to do that you
must first call this function to get the "handle" of the shader constant
that you will want to change. **NOTE** : Although a shader is made up of
two discreet programs (vertex and fragment) this function will not
differentiate between the two and will return the handle of the shader
constant from either of them.

#### Syntax:

``` gml
shader_get_uniform(shader, uniform);
```

|          |                                                                           |                                                      |
|----------|---------------------------------------------------------------------------|------------------------------------------------------|
| Argument | Type                                                                      | Description                                          |
| shader   |  [Shader Asset](../../../../../The_Asset_Editors/Shaders)             | The index of the shader to use.                      |
| uniform  |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The shader constant to get the handle of (a string). |

#### Returns:

``` gml
 Shader Uniform Handle
```

#### Example:

``` gml
shader_params = shader_get_uniform(shd_glass, "u_vRefractColour");
```

The above code will get the handle of the shader constant
"u_vRefractColour".
