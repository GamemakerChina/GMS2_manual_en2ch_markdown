# draw_get_swf_aa_level

This function can be used to get the anti-aliasing (AA) level for SWF
format vector sprites. The return value will between 0 and 1 and shows
how "smooth" the edges of these sprites will be drawn. You can set the
AA level using the function [ draw_set_swf_aa_level()
](draw_set_swf_aa_level) .

#### Syntax:

``` gml
draw_get_swf_aa_level();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if draw_get_swf_aa_level() == 0
{
    draw_enable_swf_aa(true);
    draw_set_swf_aa_level(0.5);
}
```

The above code will check the AA value for SWF format sprites, and if it
is 0 it enables AA and sets the value to 0.5.
