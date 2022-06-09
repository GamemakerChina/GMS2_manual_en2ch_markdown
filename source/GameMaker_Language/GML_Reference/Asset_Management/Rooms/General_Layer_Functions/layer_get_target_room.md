# layer_get_target_room

This function will return the current room being targeted by the layer
functions. See [ layer_set_target_room() ](layer_set_target_room)
for more information.

#### Syntax:

``` gml
layer_get_target_room()
```

#### Returns:

``` gml
 Room Asset
```

#### Example:

``` gml
if layer_get_target_room() != room
{
    layer_reset_target_room();
}
```

The above code checks the current target room and if it is not the
current room then the layer target room is reset.
