# shader_get_name

With this function you can retrieve the name of a shader resource. You
supply the unique ID value for the shader to get the name of and the
function will return the name of the resource as a string.

#### Syntax:

``` gml
shader_get_name(shader);
```

|          |                                                                |                                             |
|----------|----------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                           | Description                                 |
| shader   |  [Shader Asset](../../../../../The_Asset_Editors/Shaders)  | The index of the shader to get the name of. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
var _shader = shader_current(); var _name = shader_get_name(_shader); draw_text(32, 32, "Debug - Currently Rendering = " + _name);
```

The above code will get the name of the given shader and draw it to the
screen.
