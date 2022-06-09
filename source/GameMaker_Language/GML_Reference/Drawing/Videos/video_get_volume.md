# video_get_volume

This function returns the volume of the currently loaded video, which is
a value between 0 and 1. You can change the volume of the loaded video
using [video_set_volume()](video_set_volume) .

#### Syntax:

``` gml
video_get_volume();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
/// Step event
var _video_volume = video_get_volume();

if (_video_volume &amp;lt; 1) {
    _video_volume += 0.02;
    video_set_volume(_video_volume);
}
```

The above code would run in a Step event. It gets the volume for the
video that is currently playing, and if it's lower than 1, it will
increase it by 0.02, gradually increasing the volume until it's at the
maximum level.
