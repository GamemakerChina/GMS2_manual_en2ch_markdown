# shader_reset

This function resets the shader used for drawing and should be called
when you no longer wish to use the current shader (set using [
shader_set() ](shader_set) ).

#### Syntax:

``` gml
shader_reset();
```

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
current sprite used for the instance using it. Finally it will reset the
shader to revert to GameMaker's default shader.
