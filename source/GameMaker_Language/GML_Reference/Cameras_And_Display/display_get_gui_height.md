# display_get_gui_width

With this function you can get the height (in pixels) of the GUI as used
in the [Draw GUI
Event](../../../The_Asset_Editors/Object_Properties/Draw_Events) .

#### Syntax:

``` gml
display_get_gui_height();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
ads_move(0, display_get_gui_height() - ads_get_display_height(0), 0);
```

The above code will set an advert to display at the bottom left-hand
corner of the display.
