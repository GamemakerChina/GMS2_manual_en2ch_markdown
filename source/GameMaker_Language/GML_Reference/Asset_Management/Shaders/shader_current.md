# shader_current

This function will return the index ID value of the shader currently
being used for rendering, or it will return -1 if no shader is being
used.

#### Syntax:

``` gml
shader_current();
```

#### Returns:

``` gml
 Shader Asset

or -1 (if no shader is assigned)
```

#### Example:

``` gml
if (shader_current() == -1)
{
    shader_set(sh_warp)
}
```

The above code will check to see what the current shader is and if it
returns -1 (no shader being used) then a shader is set.
