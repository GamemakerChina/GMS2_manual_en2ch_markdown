# video_draw

This function draws the current frame of the [opened
video](video_open) to a surface (or two surfaces). It returns the
surface(s) as part of its return array, which can be [drawn
manually](../Surfaces/draw_surface) . The function also returns data
regarding the status of the video, which is expanded upon below. Ensure
that this is only called after a [video_open()](video_open) call but
before a [video_close()](video_close) call, otherwise it will not do
anything (as there will not be a video loaded).

## Return Data

The function will return an array, the first element ( \[0\] ) of which
will be a real value. This value tells the status of the video, and will
be:

-   **0** , if the video is playing without any issues
-   **-1** , if there was an error
-   On some platforms, **-2** , if the video finished playing (at which
    point it can be removed from memory with a
    [video_close()](video_close) call)
    -   It's recommended to use the [Async Callbacks](Videos#h)
        instead to know when a video ends

When this status value is **0** , the array will contain more data,
which will depend on the format of the video. You can know the video
format by calling [video_get_format()](video_get_format) .

## RGBA Videos

For RGBA videos, the position \[1\] will contain the surface where the
video frame was drawn. You can get this surface and [draw
it](../Surfaces/draw_surface) manually.

## YUV Videos

Some platforms (especially consoles) use the YUV colour format for
videos, which makes use of two surfaces. In that case the array will
have positions \[1\] and \[2\] with two surfaces:

-    \[1\] is the main video surface in black and white
-    \[2\] is the chroma surface that contains all the colour data

Both these surfaces are then combined using a YUV shader before being
used to texture a custom quad, which will draw the video to the screen.
Read [YUV Videos](YUV_Videos) for steps on drawing these two
surfaces using a shader. For the specific implementation details for a
particular console, please refer to its documentation on the [YoYo Games
Helpdesk](https://help.yoyogames.com/hc/en-us/) .

#### Syntax:

``` gml
video_draw();
```

#### Returns:

``` gml
 Array
```

#### Example:

``` gml
var _data = video_draw();
var _status = _data[0];

if (_status == 0)
{
    var _surface = _data[1];

    draw_surface(_surface, x, y);
}
```

The above code calls video_draw() , and checks if the returned status is
0, meaning the video is playing. In that case it gets the surface ID and
draws it at the instance's position. This will only work for RGBA
videos.
