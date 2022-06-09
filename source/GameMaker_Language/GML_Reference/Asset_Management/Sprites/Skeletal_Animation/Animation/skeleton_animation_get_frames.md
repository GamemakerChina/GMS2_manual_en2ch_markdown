# skeleton_animation_get_frames

This function can be used to retrieve the number of frames that any
given skeleton animation has. You supply the skeleton animation name (as
a string, as defined in the program used to make the animation, or as
returned by using the function
[skeleton_animation_get()](skeleton_animation_get) ) and the
function returns the frames that it has as an integer value. The
function will return 0 if the specified animation does not exist.

#### Syntax:

``` gml
skeleton_animation_get_frames(anim_name);
```

|           |                                                                                 |                                          |
|-----------|---------------------------------------------------------------------------------|------------------------------------------|
| Argument  | Type                                                                            | Description                              |
| anim_name |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The animation name to get the frames of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var num = skeleton_animation_get_frames(skeleton_animation_get());
image_index = num -1;
image_speed = 0;
```

The above code will get the number of frames in the animation and then
set the sprite to the last frame and stop animating.
