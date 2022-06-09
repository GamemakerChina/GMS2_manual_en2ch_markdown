# animcurve_channel_evaluate

This function can be used to get the value at a specific point in time
from a channel [struct](../../../GML_Overview/Structs) . You supply
the struct pointer for the channel (as returned by the function [
animcurve_get_channel() ](animcurve_get_channel) , or as returned in
the animation curve struct from the function [ animcurve_get()
](animcurve_get) ) and the "x" (time) position along the curve
channel to evaluate. This position should be between 0 and 1, and the
function will return the curve value at that position, or it will return
0 if the channel struct supplied is invalid.

#### Syntax:

``` gml
animcurve_channel_evaluate(channel_struct, posx);
```

|                |                                                                                                                                                 |                                                 |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument       | Type                                                                                                                                            | Description                                     |
| channel_struct |  [Animation Curve Channel Struct](../../../../../GameMaker_Language/GML_Reference/Asset_Management/Animation_Curves/animcurve_get_channel)  | The struct pointer for the channel to evaluate. |
| posx           |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                                                                          | The position in time to check (from 0 to 1).    |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _channel = animcurve_get_channel(ac_AlphaCurve, 0);
var _val = animcurve_channel_evaluate(_channel, sin(current_time/1000));
image_alpha = _val;
```

The above code gets the channel struct for the animation curve asset
"ac_AlphaCurve". It then uses the returned evaluation value to set the
image alpha for the instance.
