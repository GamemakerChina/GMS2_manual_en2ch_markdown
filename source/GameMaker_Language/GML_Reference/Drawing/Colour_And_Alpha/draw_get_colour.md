# draw_get_colour

This function returns the current draw colour which is used for drawing
forms, text, primitives and un-textured 3D models. This can be set with
the [ draw_set_colour() ](draw_set_colour) function.

#### Syntax:

``` gml
draw_get_colour()
```

#### Returns:

``` gml
 Colour
```

#### Example:

``` gml
var _cur_color = draw_get_color();
draw_set_color(text_color);
draw_text(x, y, text);
draw_set_color(_cur_color);
```

The above code stores the current draw colour into a local variable, and
changes the draw colour based on an instance variable. After drawing
some text, it resets the colour back to the value stored in the local
variable.
