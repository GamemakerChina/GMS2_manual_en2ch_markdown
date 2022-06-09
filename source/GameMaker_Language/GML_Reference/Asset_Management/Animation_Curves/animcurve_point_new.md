# animcurve_point_new

This function can be used to create a new points
[struct](../../../GML_Overview/Structs) to be added to an animation
curve channel. When created a points struct is empty and you need to set
the following variables to generate the point data:

|                                                                                                                                             |           |                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------|-----------|-------------------------------------------------------------|
|  [Animation Curve Point Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_point_new)  |           |                                                             |
| Variable Name                                                                                                                               | Data Type | Description                                                 |
|  posx                                                                                                                                       | real      | The position in time (normalised from 0 to 1) of the point. |
|  value                                                                                                                                      | real      | The value of the point.                                     |

Each point struct that you create should be added to an
[array](../../../GML_Overview/Arrays) and this is the array that is
added to the animation curve channel struct "channels" variable (as
shown in the example below).

#### Syntax:

``` gml
animcurve_point_new();
```

#### Returns:

``` gml
 Animation Curve Point Struct
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
