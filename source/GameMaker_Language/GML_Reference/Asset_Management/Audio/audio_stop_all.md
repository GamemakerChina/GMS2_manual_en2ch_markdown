# audio_stop_all

This function will stop *all* sounds that are currently playing.

#### Syntax:

``` gml
audio_stop_all();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !global.SFX
{
    audio_stop_all();
}
```

The above code checks the global variable "SFX" and if it returns false
, it will stop all sounds that are currently playing.
