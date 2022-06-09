# layer_force_draw_depth

This function forces *all* layers to be drawn at the specified z depth.
This **does not change the order the layers are rendered in** and
they'll still be drawn in depth order, it simply changes what z value is
used. In general you do not need to worry about this, but if you have
layers that have a depth outside of the legal range (-16000 to 16000)
then they won't be rendered, so you can force the Z depth to a
reasonable value - 0 for example - and they will all be rendered fine.
Note that this is generally only for use with legacy projects from
previous version of *GameMaker* where you could have draw depths higher
or lower than the permitted layer range.

#### Syntax:

``` gml
layer_force_draw_depth(force, depth)
```

|          |                                                                               |                                                                               |
|----------|-------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| Argument | Type                                                                          | Description                                                                   |
| force    |  [Boolean](../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Whether to enable (set to true or disable (set to false ) Z depth forcing     |
| depth    |  [Real](../../../../../../GameMaker_Language/GML_Overview/Data_Types)     | The new Z depth                                                               |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if !layer_is_draw_depth_forced()
{
    layer_force_draw_depth(true, 0);
}
```

The above code checks to see if the layer Z depth is forced or not and
if it is not, it sets the Z depth to 0 and enables it.
