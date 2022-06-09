# video_get_status

This function returns the status of the currently loaded video. The
status can be any one of the following constants:

|                          |                                                                                               |
|--------------------------|-----------------------------------------------------------------------------------------------|
|  Video Status Constant   |                                                                                               |
| Constant                 | Description                                                                                   |
|  video_status_closed     | No video is currently loaded, or the video was closed with [video_close()](video_close)   |
|  video_status_preparing  | The video is currently preparing and has not started playing yet                              |
|  video_status_playing    | The video is currently playing                                                                |
|  video_status_paused     | The video is paused (see [video_pause()](video_pause) )                                   |

#### Syntax:

``` gml
video_get_status();
```

#### Returns:

``` gml
Video Status Constant
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
