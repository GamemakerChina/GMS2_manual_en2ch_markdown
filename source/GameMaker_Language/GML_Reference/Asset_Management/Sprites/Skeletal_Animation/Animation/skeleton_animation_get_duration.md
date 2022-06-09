# skeleton_animation_get_duration

This function will return the time required for the given animation set
to run before looping back to the beginning. The return value is in
seconds.

#### Syntax:

``` gml
skeleton_animation_get_duration(animname);
```

|          |                                                                                 |                                                  |
|----------|---------------------------------------------------------------------------------|--------------------------------------------------|
| Argument | Type                                                                            | Description                                      |
| animname |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name (a string) of the animation set to use. |

#### Returns:

``` gml
 Real
```

#### Example1:

``` gml
time += delta_time / 1000000; var duration = skeleton_animation_get_duration(skeleton_animation_get()); var frame = floor((image_number * (mTime / duration)) + 0.5) % image_number; image_index = frame; draw_self();
```

The above code will set the image_index to the correct value for the
currently assigned skeletal animation sprite.

#### Example2:

``` gml
time += delta_time / 1000000; var d = skeleton_animation_get_duration("walk"); if time &amp;gt; d time -= d; draw_skeleton_time(sprite_index, "walk", "skin1", time, x, y, image_xscale, image_yscale, image_angle,
c_white);
```

The above code will draw the given skeletal animation sprite using
delta-time to set the frame being drawn.
