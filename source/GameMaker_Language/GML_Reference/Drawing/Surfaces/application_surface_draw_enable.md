# application_surface_draw_enable

You can use this function to enable or disable the automatic drawing of
the application surface. By default this is enabled, but in many cases
you will want to take over when and how the surface is drawn (when using
shaders for example), in which case you would use this function to set
it to false so that you can draw it yourself when and how you require.
It's important to note that when you switch off automatic drawing and
draw the application surface yourself, that you may see certain issues
with the alpha component of sprites and the surface itself. This is
because GameMaker will draw the application surface *without alpha
blending* when the automatic drawing is on. If you switch off automatic
drawing then you need to handle this yourself, using the following code
(for example):

``` gml
gpu_set_blendenable(false); draw_surface_ext(application_surface, 0, 0, 1, 1, 0, c_white, 1); gpu_set_blendenable(true);
```

#### Syntax:

``` gml
application_surface_draw_enable(flag);
```

|          |                                                                            |                                                                                    |
|----------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                                        |
| flag     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The flag will be either true (enabled, the default value) or false (disabled).     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
application_surface_draw_enable(false);
```

The above code will switch off the automatic drawing of the application
surface.
