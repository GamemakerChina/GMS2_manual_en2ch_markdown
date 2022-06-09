# display_get_gui_width

With this function you can get the width (in pixels) of the GUI as used
in the [Draw GUI
Event](../../../The_Asset_Editors/Object_Properties/Draw_Events) .

#### Syntax:

``` gml
display_get_gui_width();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
ads_move(display_get_gui_width() - ads_get_display_width(0), 0, 0);
```

The above code will set an advert to display at the top right-hand of
the display.
