# application_get_position

When you have "maintain aspect ratio" ticked in the Game Options for a
target platform, GameMaker will automatically set the draw position for
the application surface so that it is displayed correctly centered and
scaled on the given display. However if you are manipulating this
surface and wish to draw it yourself, then this function gives you an
easy way to find exactly *where* within the display or window that the
surface was being drawn so that you can then draw it there yourself, or
align GUI images or post draw images to it. The function will return an
[array](../../../GML_Overview/Arrays) with four keys, where key 0
and 1 are the x and y position of the top lefthand corner of the
surface, and keys 2 and 3 are the x and y of the bottom righthand corner
of the surface, all relative to the size of the display or window.

#### Syntax:

``` gml
application_get_position();
```

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var a = application_get_position(); xx = a[0]; yy = a[1]; ww = a[2] - a[0]; hh = a[3] - a[1];
```

The above code will get the position of the application surface, as well
as the absolute width and height in relation to the display window, and
store them in four variables for future use.
