# view_wport

This variable can be used to get or to set the width of the specified
view port. The width of the view port (or combined view ports if more
than one are active) define the width of the game window or background
canvas *at the start of the game* , so changing this value after the
game has started will have no visible effect on the game window size
unless called along with the function [ window_set_size()
](../The_Game_Window/window_set_size) . If you have a larger or
smaller port size than that assigned to the camera, then the camera view
will be scaled down - or up - to fit, as illustrated by the image
below.  
![](https://gms.magecorn.com/Manual/assets/Images/Scripting_Reference/GML/Reference/Cameras_Display/View_wh.png)  

#### Syntax:

``` gml
view_wport[0 ... 7];
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
camera_set_view_size(view_camera[0], view_wport[0], view_hport[0]);
```

The above code sets the width and height of the camera view to be the
same as the width and height of the view port.
