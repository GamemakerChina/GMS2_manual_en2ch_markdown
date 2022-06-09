# mouse_y

This **read-only** variable returns the current y axis position of the
mouse within the room.

#### Syntax:

``` gml
mouse_y;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
y = median(64, mouse_y, room_height - 64);
```

The above code will maintain the instance at the mouse y position as
long as it is within the limits of 64 pixels from the top and bottom of
the room.
