# animcurve_get_channel_index

This function will return the index value for any given animation curve
channel. You supply the animation curve ID or struct, where the curve ID
is the name of the animation curve as it was defined in the Asset
Browser, or the struct pointer as returned by the function
[animcurve_create()](animcurve_create) . You then supply the name of
the channel, as a string, and the function will return the index value
associated with that channel. Note that if the curve or channel does not
exist then you will get an error.

#### Syntax:

``` gml
animcurve_get_channel_index(curve_struct_or_id, channel_name);
```

|                    |                                                                                                                                 |                                                           |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Argument           | Type                                                                                                                            | Description                                               |
| curve_struct_or_id |  [Animation Curve Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get)  | The ID or struct pointer of the animation curve to target |
| channel_name       |  [String](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                        | The channel name (a string).                              |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _channelindex = animcurve_get_channel_index(ac_ButtonTween, "x_pos")
var _channeldata = animcurve_get_channel(ac_ButtonTween, _channelindex);
var _points = _channeldata.points;
for (var i = 0; i &amp;lt; array_length(_points); ++i;)
{
    _points[i].value += 1;
}
```

The above code retrieves the channel struct for the channel named
"x_pos" in the curve asset "ac_ButtonTween", then loops through the
points on the channel curve and adds one to their value.
