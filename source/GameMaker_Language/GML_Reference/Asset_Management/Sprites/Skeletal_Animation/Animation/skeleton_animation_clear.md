# skeleton_animation_clear

This function will clear the specified animation track of all
animations, ready to be re-assigned.

#### Syntax:

``` gml
skeleton_animation_clear(track);
```

|          |                                                                               |                               |
|----------|-------------------------------------------------------------------------------|-------------------------------|
| Argument | Type                                                                          | Description                   |
| track    |  [Real](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The animation track to clear. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if mouse_check_button(mb_right)
{
    skeleton_animation_clear(1);
}
```

The above code will clear the animation track 1 if the right mouse
button is pressed.
