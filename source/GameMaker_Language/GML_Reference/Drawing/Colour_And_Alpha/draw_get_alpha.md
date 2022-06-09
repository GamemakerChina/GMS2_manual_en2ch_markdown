# draw_get_alpha

This function returns the current value of the draw alpha, which will
range between 0 (fully transparent) and 1 (fully opaque). The draw alpha
affects the transparency of all draw functions, and can be set with the
[draw_set_alpha()](draw_set_alpha) function.

#### Syntax:

``` gml
draw_get_alpha()
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _cur_alpha = draw_get_alpha();
draw_set_alpha(text_alpha);
draw_text(x, y, text);
draw_set_alpha(_cur_alpha);
```

The above code stores the current draw alpha into a local variable, and
changes the draw alpha based on an instance variable. After drawing some
text, it resets the alpha back to the value stored in the local
variable.
