# video_resume

This function resumes the video file that is currently loaded. It must
have been paused with [video_pause()](video_pause) before calling
this function.

#### Syntax:

``` gml
video_resume();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
var _status = video_get_status();

if (keyboard_check_pressed(vk_space))
{
    if (_status == video_status_playing)
    {
        video_pause();
    }
    else if (status == video_status_paused)
    {
        video_resume();
    }
}
```

The above code gets the status of the video and then checks if the
player has pressed Space. In that case it pauses the video if it's
playing, and resumes it if it's paused.
