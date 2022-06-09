# skeleton_animation_get_ext

A single skeletal animation sprite can have various animation sets, and
these sets can be assigned different tracks so that you can "mix and
match" animation sets. This function will return the name of the
animation set currently used by the given track number (as set by the
function [ skeleton_animation_set_ext ](skeleton_animation_set_ext)
).

#### Syntax:

``` gml
skeleton_animation_get_ext(track);
```

|          |                                                                               |                                                    |
|----------|-------------------------------------------------------------------------------|----------------------------------------------------|
| Argument | Type                                                                          | Description                                        |
| track    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The track number to get the animation set name of. |

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if skeleton_animation_get_ext(1) != "bodyfight"
{
    skeleton_animation_set_ext("bodyfight", 1);
}
```

The above code will change the animation set being used by track 1 to
"bodyfight" if it is not already.
