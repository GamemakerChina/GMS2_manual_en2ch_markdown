# draw_primitive_begin

This function must be called before you can define any primitives. There
are 6 types of primitives you can define as the following constants:

|                                                                                                                          |                  |
|--------------------------------------------------------------------------------------------------------------------------|------------------|
|  [Primitive Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/draw_primitive_begin)  |                  |
| Constant                                                                                                                 | Description      |
|  pr_pointlist                                                                                                            | A point list     |
|  pr_linelist                                                                                                             | A line list      |
|  pr_linestrip                                                                                                            | A line strip     |
|  pr_trianglelist                                                                                                         | A triangle list  |
|  pr_trianglestrip                                                                                                        | A triangle strip |
|  pr_trianglefan                                                                                                          | A triangle fan   |

The following image illustrates basically how these should look and also
the order in which you should define the vertexes:  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Drawing/primitive_types.png)  
Please note that on some platforms (Windows, UWP, XBox) the
pr_trianglefan type is not natively supported and so GameMaker does a
conversion when the game is compiled to make them work. This means that
on those platforms the pr_trianglefan type will be much slower to use
than the others. This Also note that to use this function on HTML5, you
*must* enable WebGL in the Game Options.

#### Syntax:

``` gml
draw_primitive_begin(kind)
```

|          |                                                                                                                          |                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| Argument | Type                                                                                                                     | Description                                  |
| kind     |  [Primitive Type Constant](../../../../../GameMaker_Language/GML_Reference/Drawing/Primitives/draw_primitive_begin)  | The kind of primitive you are going to draw. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _steps = 20;
var _xx = 50;
var _yy = 50;
var _radius = 30;
draw_primitive_begin(pr_trianglefan);
draw_vertex(_xx, _yy);
for(var i = 0; i &amp;lt;= _steps; ++i;)
{
    draw_vertex(_xx + lengthdir_x(_radius, 270 * i / _steps), _yy + lengthdir_y(_radius, 270 * i / _steps));
}
draw_primitive_end();
```

The above code will draw three quarters of a circle made from
primitives.
