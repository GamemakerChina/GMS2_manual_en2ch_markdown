# audio_set_listener_mask

When using multiple listeners on a system, you can set the bit-mask for
a sound and have it heard from the flagged listener only. However, you
can also set the *global* mask using this function and all sounds played
normally will be heard from the listeners flagged by this mask, without
the need to set the mask for each sound individually.

#### Syntax:

``` gml
audio_set_listener_mask(mask);
```

|          |                                                                            |                                            |
|----------|----------------------------------------------------------------------------|--------------------------------------------|
| Argument | Type                                                                       | Description                                |
| mask     |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The bit-mask data to set for the listeners |

#### Returns:

``` gml
N/A
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
