# gif_open

With this function you can create an empty GIF format image, ready to
have data added to it. When you call the function, you need to specify
the width and height of the GIF (in pixels, and there is no upper limit
on size except for available memory), and the function will return the
unique ID value used to identify the gift in subsequent functions, or it
will return -1 if the gif could not be initialized (for example, if the
width/height are too big for the memory available). You may also specify
an optional argument to set the "clear colour" for the GIF. This is an
RGB value (no alpha component), and will clear the gif to this colour
before anything is added to it. If you do not supply a clear colour
argument, the default colour of black will be used. Note that when using
this function you must call [ gif_save() ](gif_save) to end the
creation of the GIF before open another file for recording (so for every
gif_open() there must be an accompanying gif_save() ).

#### Syntax:

``` gml
gif_open(width, height, [clear_colour]);
```

|                  |                                                                                                        |                                                 |
|------------------|--------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Argument         | Type                                                                                                   | Description                                     |
| width            |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The width of the gif to create                  |
| height           |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)                                    | The height of the gif to create                 |
| \[clear_colour\] |  [Colour](../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)  |  OPTIONAL The colour (RGB) to clear the gif to  |

#### Returns:

``` gml
 GIF ID
```

#### Example:

``` gml
if save_gif == true
{
    if count == 0
    {
        gif_image = gif_open(room_width, room_height);
    }
    else if count &amp;lt; 30
    {
        gif_add_surface(gif_image, application_surface, 6/100);
    }
    else
    {
        gif_save(gif_image, "GameCapture.gif");
        count = 0;
        save_gif = false;
    }
    count++;
}
```

The above code will create a GIF image file with 30 frames taken from
the application surface and then save it.
