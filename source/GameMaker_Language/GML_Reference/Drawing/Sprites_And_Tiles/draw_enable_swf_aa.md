# draw_enable_swf_aa

With this function you can enable or disable anti-aliasing (AA) for SWF
format vector sprites. AA simply smooths the edges of vector images to
give them a nicer look. The amount of AA used will depend on the value
set using the function [ draw_set_swf_aa_level()
](draw_set_swf_aa_level) . By default this is disabled.

#### Syntax:

``` gml
draw_enable_swf_aa(enable);
```

|          |                                                                            |                                                                  |
|----------|----------------------------------------------------------------------------|------------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                      |
| enable   |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Enable ( true ) or disable ( false ) AA for all SWF sprites.     |

#### Returns:

``` gml
N/A
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
