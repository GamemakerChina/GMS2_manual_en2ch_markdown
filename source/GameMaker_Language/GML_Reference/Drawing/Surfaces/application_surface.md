# application_surface

This global, built-in variable can be used to access the application
surface, for use in any of the [surface functions](Surfaces) . This
surface is permanently available and is where the game is drawn by
GameMaker . The regular Draw events ( *Draw Begin* , *Draw* and *Draw
End* ) draw to this surface by default. Other Draw events (like
*Pre/Post Draw* and *Draw GUI* ) do not draw on the application surface.
See [Draw
Events](../../../../The_Asset_Editors/Object_Properties/Draw_Events)
for more information on how those events work.

#### Syntax:

``` gml
application_surface;
```

#### Returns:

``` gml
 Surface ID
```

#### Example:

``` gml
surface_resize(application_surface, display_get_gui_width(), display_get_gui_height())
```

The above code will resize the application surface to have a 1:1 ratio
with the GUI layer.
