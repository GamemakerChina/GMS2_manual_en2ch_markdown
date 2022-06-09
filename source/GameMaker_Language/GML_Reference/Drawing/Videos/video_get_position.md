# video_get_position

This function returns the current position of the loaded video, in
milliseconds. This indicates how much the video has played, out of its
whole [duration](video_get_duration) .

#### Syntax:

``` gml
video_get_position();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (keyboard_check_pressed(vk_right))
{
    var _video_position = video_get_position();
    _video_position += 2000;

    if (_video_position &amp;lt; video_get_duration()) 
    {
        video_seek_to(_video_position);
    }
    else
    {
        video_close();
    }
}
```

The above code moves the playing video 2 seconds ahead, when the right
arrow key is pressed, and the new position is smaller than the video's
duration. However if it's not within the duration, the video is closed.
In this example, video_get_position() is used to return the position of
the video that is playing.
