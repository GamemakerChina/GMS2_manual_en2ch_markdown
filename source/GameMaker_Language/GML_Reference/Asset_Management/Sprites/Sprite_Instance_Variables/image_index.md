# image_index

A sprite is made up of one or more *sub-images* which can make the
sprite appear animated as they switch from one to the other, or can they
can be switched between in code to give different "states", much like a
button has in windows. If the sprite is animated, then you can get the
current frame of the animation by checking the image_index variable, or
if you want to change the state of a static sprite, you can select a new
sub-image by setting this variable to the desired sub-image of the
sprite. Please note that for changes in this variable to be visible, the
instance should have either *no* draw event (and so GameMaker will
default draw the sprite) or be drawn using one of the drawing functions
like [ draw_self() ](../../../Drawing/Sprites_And_Tiles/draw_self)
or [ draw_sprite_ext()
](../../../Drawing/Sprites_And_Tiles/draw_sprite_ext) (by supplying
the image_index into the appropriate argument). Note that setting this
variable directly to a frame will *not* trigger any Broadcast Messages
that may be present on that frame. Also note that while using skeletal
animation sprites, you can still get and set the image_index values -
see the function [ skeleton_animation_get_duration()
](../Skeletal_Animation/Animation/skeleton_animation_get_duration)
for examples of how to do this.

#### Syntax:

``` gml
image_index;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if (image_speed &amp;gt; 0)
{
    if (image_index &amp;gt;= image_number - 1) instance_destroy();
}
```

The above code checks to see if the sprite is animating, and if it is
then it checks to see if the current image_index is at the last frame
and in that case destroys the instance.
