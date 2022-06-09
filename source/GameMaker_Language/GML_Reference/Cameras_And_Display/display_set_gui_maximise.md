# display_set_gui_maximise

This function can be used to maximise the GUI layer and set it to be
scaled and offset in relation to the screen dimensions, rather than the
default application surface position and dimensions. By default, the GUI
layer is 1:1 with the application surface resolution and drawn at the
(0,0) position of the surface too. However this is not always what you
want and so you can use this function to set it to be drawn relative to
the absolute (0,0) position of the display or game window. What
arguments you provide to this function will depend on the effect you
wish it to have on the GUI layer. Simply calling the function with no
arguments will set the GUI layer to be drawn at the (0,0) position of
the screen or game window, with the width and height being scaled to fit
the whole area:

``` gml
display_set_gui_maximise();
```

However, you can set the *scaling factor* for the GUI layer, and the
width and height will be scaled by that amount. Remember that the GUI
layer is always made to fit the size of the display or game window, or
the application surface, so setting this value to anything other than 1
basically scales the pixel count along the width and height. If your
display is 1024x768 and you set the scaling factor to scale by 0.5, then
your GUI layer will be half the size of the display, effectively
doubling the pixel size:

``` gml
display_set_gui_maximise(0.5, 0.5);
```

Setting the values in this way will also set the draw position to the
(0,0) of the display or game window, so you can provide offset values to
"move" the (0,0) position:

``` gml
var pos = application_get_position();
display_set_gui_maximise(0.5, 0.5, pos[0], pos[1]);
```

Finally, you can reset the GUI layer using this function by setting the
scaling factors to -1. This will set the GUI layer to have a 1:1 scale
again and set the draw position to the (0,0) position of the application
surface rather than the display or window.

``` gml
display_set_gui_maximise(-1, -1);
```

#### Syntax:

``` gml
display_set_gui_maximise(

 xscale, yscale, xoffset, yoffset

);
```

|          |                                                                      |                                                                        |
|----------|----------------------------------------------------------------------|------------------------------------------------------------------------|
| Argument | Type                                                                 | Description                                                            |
| xscale   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  OPTIONAL The horizontal scaling factor (use -1 to reset to default).  |
| yscale   |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  OPTIONAL The vertical scaling factor (use -1 to reset to default).    |
| xoffset  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  OPTIONAL The x offset position for drawing.                           |
| yoffset  |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  |  OPTIONAL The y offset position for drawing.                           |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
display_set_gui_size(display_get_width() / 2, display_get_height() / 2);
display_set_gui_maximise(2, 2, 0, 0);
```

The above code will lock the draw GUI event to the given width and
height, scaling all components to fit the display, using that
proportion.
