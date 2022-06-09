# draw_self

This function draws the sprite assigned to the instance exactly as it
would be drawn if the draw event held no code or actions, and will
reflect and changes that have been made to the [sprite
variables](../../Asset_Management/Sprites/Sprite_Instance_Variables/Sprite_Instance_Variables)
in other events. **NOTE** : If the instance has no sprite assigned to
it, this function will throw an error!

#### Syntax:

``` gml
draw_self();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
draw_self();
```

This makes the instance draw itself with the properties defined by the
in built sprite variables.
