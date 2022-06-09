# skeleton_animation_mix

You can switch animation sets easily using the [
skeleton_animation_set() ](skeleton_animation_set) function, but
this may cause a skip or stutter as one animation is swapped for
another. To prevent this, you can set the mix value between two
animation sets and the sprite will interpolate between them. Normally
you would want to do this in the Create Event of the instance with the
skeletal animation as it only needs set once, and GameMaker will
interpolate all further changes to the sprite using the animation sets
in that instance. Note that the duration value is from 0 to 1, where a
value of 0.5 would have a "half and half" interpolation from one set to
the other. NOTE Spine 4.0 changes how rotational animation works, as it
no longer interpolates rotation using the shortest route possible, but
uses the absolute values in your keyframes for interpolation. This may
cause unexpected behaviour if you are upgrading your Spine animation
from an older version, and changes within your Spine project may be
required for rotations to behave as required.

#### Syntax:

``` gml
skeleton_animation_mix(animfrom, animto, duration);
```

|          |                                                                                 |                                                                     |
|----------|---------------------------------------------------------------------------------|---------------------------------------------------------------------|
| Argument | Type                                                                            | Description                                                         |
| animfrom |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name (a string) of the first animation set to interpolate from. |
| animto   |  [String](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The name (a string) of the second animation set to interpolate to.  |
| duration |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)    | The duration of the interpolation (from 0 to 1)                     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
skeleton_animation_set("walk");
skeleton_animation_mix("walk", "jump", 0.2);
skeleton_animation_mix("jump", "walk", 0.4);
```

The above code would go in the Create Event of an instance with a
skeletal animation sprite and sets the animation mix duration for
interpolating between the two animations sets "walk" and "jump".
