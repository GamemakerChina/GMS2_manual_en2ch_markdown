# video_is_looping

This function returns whether the currently loaded video is set to loop
( true ) or not ( false ). You can set a video to loop by calling
[video_enable_loop()](video_enable_loop) .

#### Syntax:

``` gml
video_is_looping();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (video_is_looping()) {
    obj_player.control_enabled = false;
}
```

The above code checks if the currently loaded video is looping, and in
that case, disables the player's controls, by setting a custom instance
variable to false .
