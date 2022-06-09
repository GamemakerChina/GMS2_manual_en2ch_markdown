# room_height

This variable holds the height of the current room in pixels. You can
change this variable to change the height of the room at any time, and
changes will be applied to the bottom of the room, as the origin is
considered to be the top left corner. So, for example, if the room is
480px in height and you set it to 640px, the room will be expanded
downwards with an extra 180px added to the bottom.

#### Syntax:

``` gml
room_height;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if bbox_bottom &amp;gt; room_height
{
    y += room_height - bbox_bottom;
}
```

The above code checks to see if the current instance's sprite bounding
box is greater than the height of the room, and if it is it moves the
instance up.
