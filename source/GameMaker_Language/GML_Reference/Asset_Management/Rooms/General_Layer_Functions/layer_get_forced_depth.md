# layer_get_forced_depth

This function can be used to retrieve the Z depth set for rendering
layers within the room. See [ layer_force_draw_depth()
](layer_force_draw_depth) for more information.

#### Syntax:

``` gml
layer_get_forced_depth()
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if layer_get_forced_depth() != 0
{
    layer_force_draw_depth(true, 0);
}
```

The above code checks to see if the layer Z depth is forced to a value
of 0 or not and if it is not, it sets the layer Z depth to 0.
