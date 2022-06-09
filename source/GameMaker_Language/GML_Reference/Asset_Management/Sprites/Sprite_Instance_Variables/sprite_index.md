# sprite_index

This variable returns the index of the current sprite for the instance,
or -1 if the instance has no sprite associated with it. You can change
it to give the instance a different sprite by giving it the name of a
sprite from the resource tree or by using a variable that has an
externally loaded sprite indexed in it. Changing the sprite does not
change the index of the currently visible frame, so if you change the
sprite on frame number 3, the new sprite will be drawn with that frame
visible (assuming it has the same number of frames).

#### Syntax:

``` gml
sprite_index;
```

#### Returns:

``` gml
 Sprite Asset
```

#### Example:

``` gml
with (obj_Check)
{
    if !collision_line(x, y, other.x, other.y, obj_Wall, false, true)
    {
        sprite_index = spr_spotted;
    }
    else
    {
        sprite_index = spr_clear;
    }
}
```

The above code will loop through all instances of "obj_Check" checking
for a collision line between them and the instance running the code. The
sprite of those instances will be changed depending on the return value
(true or false) for the collision line.
