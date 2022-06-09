# timeline_speed

Normally, in each step the position in the time line is increased by 1,
however you can change this amount by setting this variable to a
different value. You can use real numbers (like 0.5, or 2.4 for example)
and if the value is larger than one, several moments can happen within
the same time step (they will all be performed in the same order as
defined for the time line, so no actions will be skipped).

#### Syntax:

``` gml
timeline_speed;
```

#### Returns:

``` gml
 Real

(single precision floating point value)
```

#### Example:

``` gml
if !timeline_running
{
    timeline_running = true;
    timeline_speed = 0.5;
}
```

The above code will check and see if the instance is running its
associated time line and if it is not, it will start the time line
running at half speed.
