# audio_listener_get_data

This function will create a [DS
map](../../../Data_Structures/DS_Maps/DS_Maps) and populate it with
the position, velocity and orientation values for the given listener.
The default listener index is 0, but you can use the function [
audio_get_listener_info() ](audio_get_listener_info) to get the
different indices available for the target platform. If you provide an
incorrect listener index then the function will return -1. ** NOTE **
You are responsible for the destruction of the returned DS map using the
appropriate function. The DS map will contain the following keys:

-   " **x** " - The x position of the listener
-   " **y** " - The y position of the listener
-   " **z** " - The z position of the listener
-   " **vx** " - The x axis velocity of the listener
-   " **vy** " - The y axis velocity of the listener
-   " **vz** " - The z axis velocity of the listener
-   " **lookat_x** " - The x component of the look at vector of the
    listener
-   " **lookat_y** " - The y component of the look at vector of the
    listener
-   " **lookat_z** " - The z component of the look at vector of the
    listener
-   " **up_x** " - The x component of the up vector of the listener
-   " **up_y** " - The y component of the up vector of the listener
-   " **up_z** " - The z component of the up vector of the listener

#### Syntax:

``` gml
audio_listener_get_data(index);
```

|          |                                                                                                                                                                                                                    |                                                  |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                                                                                                                                                               | Description                                      |
| index    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The listener to get the data for (default is 0). |

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
var num = audio_get_listener_count();
for(var i = 0; i &amp;lt; num; ++i;)
{
    var info = audio_get_listener_info(i);
    var data = audio_listener_get_data(info[? "index"]);
    if data[? "x"] != 0
    {
        audio_listener_set_position(info[? "index"], 0, 0, 0);
    }
    ds_map_destroy(info);
    ds_map_destroy(data);
}
```

The above code checks the number of listeners available then loops
through them and if their x position is not 0, it sets their position to
0, 0, 0.
