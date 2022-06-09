# shader_is_compiled

This function will check a shader at run-time to make sure that it has
been successfully compiled. If it has then the function returns true
otherwise it returns false . This function should be used at the start
of the game to make sure that the platform running your game has
successfully compiled any shaders used (particularly on Windows where
some computers may be using DX9 with Shader Level 2.0 and not a later
version using shader level 3.0). If your shader has *NOT* been compiled
and you call [ shader_set() ](shader_set) the game will crash, so it
is worth while having some sort of check whenever you are using anything
other than simple GLSL ES shaders.

#### Syntax:

``` gml
shader_is_compiled(shader);
```

|          |                                                                |                      |
|----------|----------------------------------------------------------------|----------------------|
| Argument | Type                                                           | Description          |
| shader   |  [Shader Asset](../../../../../The_Asset_Editors/Shaders)  | The shader to check. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
global.GFX = false;
if (shader_is_compiled(sh_glass) &amp;amp;&amp;amp; shader_is_compiled(sh_warp))
{
    global.GFX = true;
}
```

The above code will set a global variable to false , and then if both
the shaders being checked have compiled correctly, it will be set to
true .
