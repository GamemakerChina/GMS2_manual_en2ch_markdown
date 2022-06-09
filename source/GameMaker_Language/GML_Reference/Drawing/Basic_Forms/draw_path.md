# draw_path

With this function you can get GameMaker to draw a path to the screen.
The path will be drawn as a simple line, and can be either relative to
the calling instance or at the absolute position it was created at in
the path editor or through code. This function is extremely useful when
debugging dynamic paths (for example, those created for instances with
the [ mp_grid_path()
](../../Movement_And_Collisions/Motion_Planning/mp_grid_path)
function). **NOTE** : If you are wanting to draw a shape using a shader,
you should be aware that most shaders expect the following inputs:
vertex, texture, Colour. However, when using this function, only vertex
and colour data are being passed in, and so the shader may not draw
anything (or draw something but not correctly). If you need to draw
shapes in this way then the shader should be customised with this in
mind.

#### Syntax:

``` gml
draw_path(path, x, y, absolute);
```

|          |                                                                            |                                                                                                    |
|----------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                                        |
| path     |  [Path Asset](../../../../../The_Asset_Editors/Paths)                  | The path to draw                                                                                   |
| x        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The x coordinate of where the path is drawn                                                        |
| y        |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The y coordinate of where the path is drawn                                                        |
| absolute |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether the path is drawn at the absolute position ( true ) or the relative position ( false )     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mp_grid_path(grid, path, x, y, obj_Player.x, obj_Player.y, 1)
{
    draw_path(path, x, y, false);
}
```

The above code will use the mp_grid_path function to generate a path and
store it in the variable "path". If the path is successfully created, it
is then drawn on the screen at a position relative to the instance
running the code.
