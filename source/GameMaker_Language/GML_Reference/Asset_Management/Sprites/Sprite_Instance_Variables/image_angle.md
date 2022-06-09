# image_angle

This value sets the angle (rotation) of the sprite and is measured in
degrees, with the right being 0º, up being 90º, left being 180º and down
being 270º. Set this variable to 0 to reset the sprite to be drawn as
was defined in the sprite editor. Please note that for changes in this
variable to be visible, the instance should have either *no* draw event
(and so GameMaker will default draw the sprite) or be drawn using one of
the extended drawing functions like [ draw_self()
](../../../Drawing/Sprites_And_Tiles/draw_self) or [
draw_sprite_ext()
](../../../Drawing/Sprites_And_Tiles/draw_sprite_ext) .

#### Syntax:

``` gml
image_angle;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
image_angle = point_direction(x, y, mouse_x, mouse_y);
```

The above code will rotate the sprite of the instance to always point at
the mouse position.
