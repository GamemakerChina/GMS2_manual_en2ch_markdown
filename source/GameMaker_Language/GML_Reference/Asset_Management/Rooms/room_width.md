# room_width

This variable holds the width of the current room in pixels. You can
change this variable to change the width of the room at any time.

#### Syntax:

``` gml
room_width;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if bbox_right &amp;gt; room_width
{
    x += room_width - bbox_right;
}
```

The above code checks to see if the current instance's sprite bounding
box is greater than the width of the room, and if it is it moves the
instance up.
