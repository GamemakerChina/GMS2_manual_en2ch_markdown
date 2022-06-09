# mouse_x

This **read-only** variable returns the current x axis position of the
mouse within the room.

#### Syntax:

``` gml
mouse_x;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
x = median(64, mouse_x, room_width - 64);
```

The above code will maintain the instance at the mouse x position as
long as it is within the limits of 64 pixels from either side of the
room.
