# animcurve_create

This function will create an empty animation curve
[struct](../../../GML_Overview/Structs) , ready for you to populate
with channel data. The function will return a pointer to the struct and
this is then used to add channels and other data to the animation curve.
You can also supply this to functions like [ animcurve_get()
](animcurve_get) to later get the data from the curve. When you use
this function, the struct created will have no data in it, and to use it
you should add at least one channel and the channel should have points
added to it. To add a channel, see the function [
animcurve_channel_new() ](animcurve_channel_new) , and to add points
to the channel, see the function [ animcurve_point_new()
](animcurve_point_new) . Additionally you can give the animation
curve struct a name by setting the "name" variable (as shown in the
example code, below). Channels added to a new animation curve should be
added as an [array](../../../GML_Overview/Arrays) , where each item
in the array references a channel struct, and the points in a channel
should also be added as an array, where each array item references a
point struct. Note that animation curves created in this way **must be
deleted when no longer required** as they will take up space in memory
otherwise, which may lead to a memory leak, slowing down and eventually
crashing your game. You can remove an animation curve when no longer
needed using the function [ animcurve_destroy() ](animcurve_destroy)
. You do not need to to clean up any channel or point data within the
curve, as this will be done by the garbage collector automatically when
the curve itself is destroyed.

#### Syntax:

``` gml
animcurve_create();
```

#### Returns:

``` gml
 Animation Curve Struct
```

#### Example:

``` gml
my_curve = animcurve_create();
my_curve.name = "My_Curve";
var _channels = array_create(1);
_channels[0] = animcurve_channel_new();
_channels[0].name = "alpha";
_channels[0].type = animcurvetype_catmullrom;
_channels[0].iterations = 8;
var _points = array_create(3);
_points[0] = animcurve_point_new();
_points[0].posx = 0;
_points[0].value = 0;
_points[1] = animcurve_point_new();
_points[1].posx = 0.5;
_points[1].value = 1;
_points[2] = animcurve_point_new();
_points[2].posx = 1;
_points[2].value = 0;
_channels[0].points = _points;
my_curve.channels = _channels;
```

The above code creates a new animation curve struct and stores it in the
variable "my_curve". This struct is then populated with a name and a
channel array. The channel array contains a single channel with three
points.
