# window_get_visible_rects

With this function you can find the overlapping region of the rectangle
defined by (x1,y1) to (x2,y2) on each of the attached displays. The
function will return an array with 8 values per display (ie: if you have
two displays, the array will have a length of 16 indices), where the
values \[0 ... 3\] correspond to the overlapx1, overlapy1, overlapx2,
overlapy2 - defining the region of overlap on this display and will be
set to 0,0,0,0 if no overlap - and the values \[4 ... 7\] corresponds to
the monitorx1, monitory1, monitorx2, monitory2 - the coordinates of the
display in the virtual display space. This can be used to test whether a
saved window position is going to be visible or not (the user may have
disconnected an external monitor or moved the window off screen which
left the window position that was saved as not being valid), for
example.

#### Syntax:

``` gml
window_get_visible_rects(x1, y1, x2, y2);
```

|          |                                                                         |                                            |
|----------|-------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                    | Description                                |
| x1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The left edge of the rectangle to check    |
| y1       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The top edge of the rectangle to check.    |
| x2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The right edge of the rectangle to check   |
| y2       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The bottom edge of the rectangle to check. |

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var wx = window_get_x(); var wy = window_get_y(); var ww = window_get_width(); var wh = window_get_height(); display_data = window_get_visible_rects(wx, wy, wx + ww, wy + wh); display_num = array_length(display_data) / 8;
```

The above code will generate a 1D array held in the variable
display_data containing the information about the displays, as well as
create the variable display_num to hold the number of active displays
found.
