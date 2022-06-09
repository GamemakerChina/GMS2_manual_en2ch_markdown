# cursor_sprite

Setting this variable will instruct GameMaker to use the designated
sprite as a cursor (basically setting it to the current mouse x/y
position every step). The default value is -1 which is no sprite for the
cursor, but you can assign any sprite index from the game assets or that
has been imported from an external resource. Please note that there is
no way to control the animation speed or image_index, so if the sprite
has sub-images, these will be cycled at the same speed as the room
speed. To remove the cursor sprite, you can set this variable to -1
again. It is also worth noting that this variable does *not* replace the
game window cursor, and that it will still be drawn as normal. To avoid
this you can use the function [ window_set_cursor()
](../Cameras_And_Display/The_Game_Window/window_set_cursor) and set
it to the constant cr_none which will make the standard cursor
invisible.

#### Syntax:

``` gml
cursor_sprite;
```

#### Returns:

``` gml
 Sprite Asset
```

#### Example:

``` gml
cursor_sprite = spr_CustomCursor;
```

The above code will set the sprite indexed in the variable
"spr_CustomCursor" to be the cursor sprite for the game.
