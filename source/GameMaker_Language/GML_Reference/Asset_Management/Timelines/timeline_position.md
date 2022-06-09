# timeline_position

This variable holds the current position (moment) a time line is
currently at. You can change this value to skip parts of the time line,
or to repeat parts or to start the time line again from the beginning.

#### Syntax:

``` gml
timeline_position;
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
    timeline_position = 0;
    timeline_running = true;
}
```

The above code will check to see if the instance is running a time line,
and if it is not then it resets the assigned time line to start at the
first moment and then starts it.
