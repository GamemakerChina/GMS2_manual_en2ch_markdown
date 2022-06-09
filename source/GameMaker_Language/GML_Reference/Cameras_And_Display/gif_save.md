# gif_save

With this function you can save out a GIF animation. You supply the GIF
index (as returned by the function [ gif_open() ](gif_open) ) as
well as a filename to save it with. Note that GameMaker does not
automatically append the .gif file extension, so you should include this
as part of the filename string if you wish the saved file to be
identified as a GIF. The created GIF will be palletized using the
Universal 884 Palette (see
[here](https://en.wikipedia.org/wiki/List_of_software_palettes#8-8-4_levels_RGB)
for more information). Note that if the function is successful and the
GIF is saved correctly, then it will return 0, otherwise it will return
-1.

#### Syntax:

``` gml
gif_save(gif_index, fname);
```

|           |                                                                                           |                                 |
|-----------|-------------------------------------------------------------------------------------------|---------------------------------|
| Argument  | Type                                                                                      | Description                     |
| gif_index |  [GIF ID](../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/gif_open)  | The ID of gif to save           |
| fname     |  [String](../../../../GameMaker_Language/GML_Overview/Data_Types)                     | The filename to use for the gif |

#### Returns:

``` gml
 Real
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
