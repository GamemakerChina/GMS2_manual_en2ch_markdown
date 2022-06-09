# audio_get_listener_info

This function will create a [DS
map](../../../Data_Structures/DS_Maps/DS_Maps) and populate it with
information for the given listener. ** NOTE ** You are responsible for
the destruction of the returned DS Map using the appropriate function.
The DS map will contain the following keys:

-   " **name** " - The name of the listener, as a string, with "default"
    being the standard listener name on most target platforms
-   " **mask** " - The bit-mask for the listener
-   " **index** " - The unique index value of the listener

The mask value can be used to set a sound or emitter to play from
multiple listeners at once, simply using the bitwise or "\|" to generate
a mask for the sound (see the example code below), while the index is
used to set the properties like position or velocity for a given
listener using functions like [ audio_listener_set_position()
](audio_listener_set_position) .

#### Syntax:

``` gml
audio_get_listener_info(num);
```

|          |                                                                                                                                                                                                                    |                                          |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                                                                                                                                                               | Description                              |
| num      |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types) or [Audio Listener ID](../../../../../../GameMaker_Language/GML_Reference/Asset_Management/Audio/Audio_Listeners/Audio_Listeners)    | The listener number to get the data for. |

#### Returns:

``` gml
 DS Map ID
```

#### Example:

``` gml
var num = audio_get_listener_count();
var mask = 0; for(var i = 0; i &amp;lt; num; ++i;)
{
    var info = audio_get_listener_info(i);
    var m = audio_listener_get_data(info[? "mask"]);
    mask = mask | m;
    ds_map_destroy(info);
}
audio_set_listener_mask(mask);
```

The above code checks the number of listeners available then loops
through them gets their mask bits, which are then combined to create a
single bit mask which is applied to the global listener.
