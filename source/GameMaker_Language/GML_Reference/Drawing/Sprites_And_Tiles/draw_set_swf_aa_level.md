# draw_set_swf_aa_level

This function can be used to set the anti-aliasing (AA) level for SWF
format vector sprites. This can be a real value from 0 to 1 and will
"smooth" the edges of these sprites. Note that to see this effect, you
must first have enabled AA using the function [ draw_enable_swf_aa()
](draw_enable_swf_aa) .

#### Syntax:

``` gml
draw_set_swf_aa_level(AA);
```

|          |                                                                         |                                             |
|----------|-------------------------------------------------------------------------|---------------------------------------------|
| Argument | Type                                                                    | Description                                 |
| AA       |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The anti-aliasing value to use from 0 to 1. |

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
