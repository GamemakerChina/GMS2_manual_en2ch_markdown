# animcurve_get

This function will return a [struct](../../../GML_Overview/Structs)
containing all the data for the given animation curve. You supply the
animation curve asset ID (as defined in the Asset Browser), and the
function will return a struct with the following variables:

|                                                                                                                                 |                                                                                                                                                                                                                           |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
|  [Animation Curve Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get)  |                                                                                                                                                                                                                           |                                                                     |
| Variable Name                                                                                                                   | Data Type                                                                                                                                                                                                                 | Description                                                         |
|  name                                                                                                                           |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                                                                                                  | This is the name of the animation curve.                            |
|  channels                                                                                                                       |  [Array](../../../../../GameMaker_Language/GML_Overview/Arrays) of [Animation Curve Channel Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get_channel) s    | This is an array, where each item in the array is a channel struct. |

The channels variable in the struct is an
[array](../../../GML_Overview/Arrays) where each array item is an
[Animation Curve Channel
Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get_channel)
with data relating to a channel within the curve. The channel struct is
explained [on this page](animcurve_channel_new) . As with channels,
the points on a single channel are stored as structs in an array, where
each item in the array is a single point struct. The point struct is
explained [on this page](animcurve_point_new) . Note that if the
function fails (e.g. the given Animation Curve asset does not exist)
then the function will return -1.

#### Syntax:

``` gml
animcurve_get(curve_id);
```

|          |                                                                                  |                                                             |
|----------|----------------------------------------------------------------------------------|-------------------------------------------------------------|
| Argument | Type                                                                             | Description                                                 |
| curve_id |  [Animation Curve Asset](../../../../../The_Asset_Editors/Animation_Curves)  | The asset browser ID (index) of the animation curve to get. |

#### Returns:

``` gml
 Animation Curve Struct

or -1
```

#### Example:

``` gml
var _curve = animcurve_get(ac_ButtonTween);
var _channel = _curve.channels[0];
if _channel.type != animcurvetype_linear
{
    _channel.type = animcurvetype_linear;
}
```

The above code retrieves the animation curve struct for the curve asset
"ac_ButtonTween", then checks the curve type for the first channel, and
if it's not linear it sets it to linear.
