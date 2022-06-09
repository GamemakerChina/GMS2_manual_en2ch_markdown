# video_close

This function closes the video file that is currently loaded. Ensure
that this is only called after a [video_open()](video_open) call,
otherwise it will not do anything.

#### Syntax:

``` gml
video_close();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (keyboard_check_pressed(vk_escape))
{
    video_close();
}
```

The above code closes the video when the Escape key is pressed.
