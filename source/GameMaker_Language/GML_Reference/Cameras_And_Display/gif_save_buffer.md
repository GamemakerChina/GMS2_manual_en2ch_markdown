# gif_save_buffer

With this function you can save out a GIF animation. You supply the GIF
index (as returned by the function [ gif_open() ](gif_open) ) and
the function will return a 1 byte-aligned grow buffer with the GIF data.
Note that the final GIF data will have been palletized using the
Universal 884 Palette (see
[here](https://en.wikipedia.org/wiki/List_of_software_palettes#8-8-4_levels_RGB)
for more information).

#### Syntax:

``` gml
gif_save_buffer(gif_index);
```

|           |                                                                                           |                       |
|-----------|-------------------------------------------------------------------------------------------|-----------------------|
| Argument  | Type                                                                                      | Description           |
| gif_index |  [GIF ID](../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/gif_open)  | The ID of gif to save |

#### Returns:

``` gml
 Buffer ID
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
        global.capture_buff = gif_save_buffer(gif_image);
        count = 0;
        save_gif = false;
    }
    count++;
}
```

The above code will create a GIF image file with 30 frames taken from
the application surface and then save it to a buffer.
