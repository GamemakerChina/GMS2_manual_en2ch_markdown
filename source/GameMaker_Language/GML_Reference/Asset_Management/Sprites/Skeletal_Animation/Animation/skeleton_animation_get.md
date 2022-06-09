# skeleton_animation_get

With this function you can get the current animation set being used by
your skeletal animation sprite. The return value is a string, which will
be the name of the set as you defined it in your skeletal animation
program.

#### Syntax:

``` gml
skeleton_animation_get();
```

#### Returns:

``` gml
 String
```

#### Example:

``` gml
if keyboard_check_pressed(vk_space)
{
    if skeleton_animation_get() != "jump"
    {
        skeleton_animation_set("jump");
    }
}
```

The above code will change the animation set being used to the "jump"
set when the space key is pressed, but only if the current set being
used is not already "jump".
