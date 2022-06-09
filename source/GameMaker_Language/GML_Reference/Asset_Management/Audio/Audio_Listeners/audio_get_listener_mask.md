# audio_get_listener_mask

This function will return the bit-mask data that defines the current
default (global) mask for the audio listeners.

#### Syntax:

``` gml
audio_get_listener_mask();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var g_mask = audio_get_listener_mask();
if g_mask != global.Audio_Mask
{
    var num = audio_get_listener_count();
    global.Audio_Mask = 0;

    for(var i = 0; i &amp;lt; num; ++i;)
    {
        var info = audio_get_listener_info(i);
        var m = audio_listener_get_data(info[? "mask"]);
        global.Audio_Mask = global.Audio_Mask | m;
        ds_map_destroy(info);
    }
    audio_set_listener_mask(mask);
}
```

The above code gets the current listener mask data and compares it to
the data stored in a global variable. If they are not the same, the code
checks the number of listeners available then loops through them and
gets their mask bits, which are then combined to create a single mask
which is applied to the audio system to define the global listeners.
