# skeleton_animation_get_frame

This function will return the frame number of the animation on the
specified animation track. The function will return -1 if no animation
is assigned to the specific track given.

#### Syntax:

``` gml
skeleton_animation_get_frame(track);
```

|          |                                                                               |                                          |
|----------|-------------------------------------------------------------------------------|------------------------------------------|
| Argument | Type                                                                          | Description                              |
| track    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The animation track to get the frame of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var frame = skeleton_animation_get_frame(0);
if frame &amp;gt; 0 &amp;amp;&amp;amp; frame &amp;lt; 2
{
    var box = skeleton_get_minmax();
    var ww = (box[2] - box[0]) / 2;
    var hh = (box[3] - box[1]) / 2;
    part_particles_create(global.p_sys, box[0] + ww, box[1] + hh, global.Stars, 10);
}
```

The above code will check the current frame of the animation assigned to
track 0 and then burst some particles from a point in the middle of the
total bounding box for the sprite.
