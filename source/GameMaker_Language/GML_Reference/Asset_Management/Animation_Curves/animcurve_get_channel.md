# animcurve_get_channel

This function will return the
[struct](../../../GML_Overview/Structs) containing the channel data
for the channel specified in an animation curve asset. You supply the
animation curve ID or struct as well as the channel name or index, and
the function will return a struct with the following format:

|               |                                                                                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Variable Name | Data Type                                                                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                           |
|  name         | string                                                                                                                                                       | This is the name of the channel.                                                                                                                                                                                                                                                                                                                                                                      |
|  type         |  [Animation Curve Interpolation Type Constant](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_channel_new)  | This will be one of the constants **animcurvetype_linear** for linear interpolation between points, **animcurvetype_catmullrom** for "smooth" interpolation between the points using catmull-rom interpolation, or animcurvetype_bezier for Bezier interpolation.                                                                                                                                     |
|  iterations   | integer                                                                                                                                                      | If the channel is using catmull-rom ("smooth") interpolation this holds how many points have been generated for each segment of the curve (note that these extra points are internal to the function and only used for the runtime calculations). If the channel is using linear interpolation, this value will still exist but can be ignored as it has no bearing on how the curve is interpolated. |
|  points       | array pointer                                                                                                                                                | This is an array, where each item in the array is a point struct.                                                                                                                                                                                                                                                                                                                                     |

The animation curve ID is the name of the animation curve as it was
defined in the Asset Browser, or the struct pointer as returned by the
function [ animcurve_create() ](animcurve_create) . The channel name
is a string which refers to the channel as it was defined in the
Animation Curve asset, or you can supply an index value, which is from 0
to *n* , where *n* is the last channel in the curve asset (eg: if an
animation curve has 4 channels, they will be indexed from 0 to 3). Note
that passing an index value will require less processing than passing in
a channel name. If the function fails (ie: no channel exists with the
given name or index) then you will get an error. The points on a single
channel are stored as structs in an
[array](../../../GML_Overview/Arrays) , where each item in the array
is a single point struct. The point struct has the following variables:

|               |           |                                                             |
|---------------|-----------|-------------------------------------------------------------|
| Variable Name | Data Type | Description                                                 |
|  posx         | real      | The position in time (normalised from 0 to 1) of the point. |
|  value        | real      | The value of the point.                                     |

#### Syntax:

``` gml
animcurve_get_channel(curve_struct_or_id, channel_name_or_index);
```

|                       |                                                                                                                                                      |                                                                |
|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument              | Type                                                                                                                                                 | Description                                                    |
| curve_struct_or_id    |  [Animation Curve Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get)                       | The ID or struct pointer of the animation curve to target      |
| channel_name_or_index |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The channel name (a string) or the channel index (an integer). |

#### Returns:

``` gml
 Animation Curve Channel Struct
```

#### Example:

``` gml
var _channeldata = animcurve_get_channel(ac_ButtonTween, 0);
var _points = _channeldata.points;
for (var i = 0; i &amp;lt; array_length(_points); ++i;)
{
    _points[i].value += 1;
}
```

The above code retrieves the channel struct for channel 0 in the curve
asset "ac_ButtonTween", then loops through the points on the channel
curve and adds one to their value.
