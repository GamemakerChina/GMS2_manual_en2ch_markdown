# video_seek_to

This function allows you to seek to the given position in the currently
loaded video. You specify the time value to seek to, which is in
milliseconds. This function works best when the video is paused, and the
distance from the current position to the new seek position is not too
small.

#### Syntax:

``` gml
video_seek_to(time);
```

|          |                                                                         |                                        |
|----------|-------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                    | Description                            |
| time     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The time to seek to (in milliseconds). |

#### Returns:

``` gml
N/A
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
In this example, video_seek_to() is used to seek the video to the new
position.
