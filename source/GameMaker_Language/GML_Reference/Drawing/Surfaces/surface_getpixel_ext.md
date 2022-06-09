# surface_getpixel_ext

With this function you can get the full **abgr 32bit** value of any
pixel of a (previously created) surface. **NOTE** : This function will
have a huge performance hit and so should only be used when absolutely
necessary.

#### Syntax:

``` gml
surface_getpixel_ext(surface_id, x, y);
```

|            |                                                                                                     |                                        |
|------------|-----------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument   | Type                                                                                                | Description                            |
| surface_id |  [Surface ID](../../../../../GameMaker_Language/GML_Reference/Drawing/Surfaces/surface_create)  | The ID of the surface to use.          |
| x          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The x coordinate of the pixel to check |
| y          |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)                              | The y coordinate of the pixel to check |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
col = surface_getpixel_ext(mouse_x, mouse_y); alpha = (col &amp;gt;&amp;gt; 24) &amp;amp; 255; blue = (col &amp;gt;&amp;gt; 16) &amp;amp; 255; green = (col &amp;gt;&amp;gt; 8) &amp;amp; 255; red = col &amp;amp; 255;
```

The above code will get the 32bit colour value at the position of the
mouse and then split it into its component values, storing them in
variables.
