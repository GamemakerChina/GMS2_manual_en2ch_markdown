# skeleton_animation_get_event_frames

This function can be used to retrieve all the frames for the given
event, in the given animation. You supply the skeleton animation name
(as a string, as defined in the program used to make the animation, or
as returned by using the function
[skeleton_animation_get()](skeleton_animation_get) ) and an event
name. The function returns an array with the frames for that event. If
the specified event name does not exist, the function will return an
array with **-1** as its first (and only) element.

#### Syntax:

``` gml
skeleton_animation_get_event_frames(anim_name, event_name);
```

|            |                                                                                 |                                          |
|------------|---------------------------------------------------------------------------------|------------------------------------------|
| Argument   | Type                                                                            | Description                              |
| anim_name  |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The animation name to get the frames of. |
| event_name |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The event name to get the frames for.    |

#### Returns:

``` gml
 Array

of

 Real

s
```

#### Example:

``` gml
var _frames = skeleton_animation_get_event_frames(skeleton_animation_get(), "Footstep");

if (_frames[0] != -1)
{
    var _count = array_length(_frames);
    var _current_frame = skeleton_animation_get_frame(0);

    for (var i = 0; i &amp;lt; _count; i ++)
    {
        if (_frames[i] == _current_frame)
        {
            audio_play_sound(snd_footstep, 1, false);
            break;
        }
    }
}
```

The above code gets the frames for the "Footstep" event. If it returned
an array with the valid frames, it loops through it, and checks if the
current frame is equal to any of the frames in the array. In that case
it plays the footstep sound effect and breaks (stops) the loop.
