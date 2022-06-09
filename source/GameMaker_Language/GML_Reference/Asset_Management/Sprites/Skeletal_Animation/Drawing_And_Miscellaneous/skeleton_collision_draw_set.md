# skeleton_collision_draw_set

With this function, you can toggle on ( true ) or off ( false ) drawing
the collision data for the current skeletal animation sprite being used
by the instance. If this is switched on, the bounding box and the
precise collision mask will be drawn as outlines around the sprite. This
function only works when the skeletal sprite drawing is being handled by
the object. To draw the collision bounding box when drawing a skeletal
sprite manually, use
[draw_skeleton_collision()](draw_skeleton_collision) . NOTE The
bounding box of a Spine sprite is set up in Spine itself, not in
GameMaker .

#### Syntax:

``` gml
skeleton_collision_draw_set(flag);
```

|          |                                                                                  |                                                               |
|----------|----------------------------------------------------------------------------------|---------------------------------------------------------------|
| Argument | Type                                                                             | Description                                                   |
| flag     |  [Boolean](../../../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Set to true to turn on drawing, and false to turn it off.     |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if debug_mode == true
{
    skeleton_collision_draw_set(true);
}
```

The above code checks to see if the game is being run in debug mode and
if it is, it toggles the skeletal collision data for the instance to be
shown.
