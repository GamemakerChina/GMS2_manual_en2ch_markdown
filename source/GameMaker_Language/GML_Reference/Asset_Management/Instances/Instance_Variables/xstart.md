# xstart

This variable stores the initial x position of the instance when it is
first created in the room. This is not a read-only variable and can be
set as well as read.

#### Syntax:

``` gml
xstart;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if place_meeting(x, y, obj_spike)
{
    score -= 100;
    x = xstart;
    y = ystart;
}
```

The above code will check for a collision with an instance of
"obj_spike" and if there is one, it deducts 100 from the score and moves
the instance back to its starting position.
