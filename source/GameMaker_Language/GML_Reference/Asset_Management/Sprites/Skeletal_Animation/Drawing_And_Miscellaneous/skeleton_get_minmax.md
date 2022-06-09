# skeleton_get_minmax

This function will return an array with the total bounding box value for
all the individual bounding boxes assigned to a skeleton animation
sprite. The returned array will have 4 elements:

-   \[0\] - the minimum x position for all bounding boxes
-   \[1\] - the minimum y position for all bounding boxes
-   \[2\] - the maximum x position for all bounding boxes
-   \[3\] - the maximum y position for all bounding boxes

NOTE The bounding box of a Spine sprite is set up in Spine itself, not
in GameMaker .

#### Syntax:

``` gml
skeleton_get_minmax();
```

#### Returns:

``` gml
 Array

(4 elements: xMin, yMin, xMax, yMax)
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
