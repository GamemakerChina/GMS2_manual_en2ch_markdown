# layer_is_draw_depth_forced

This function can be used to check and see whether forced Z depth is
enabled for rendering the layers in the project. See [
layer_force_draw_depth() ](layer_force_draw_depth) for more
information.

#### Syntax:

``` gml
layer_is_draw_depth_forced()
```

#### Returns:

``` gml
 Boolean
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
