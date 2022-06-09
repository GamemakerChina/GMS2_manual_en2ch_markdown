# gc_get_target_frame_time

With this function you can retrieve the current target frame value for
the garbage collector. The value returned is in microseconds (where
1,000,000 microseconds equals one second) and the default target frame
time is 100 microseconds. If you wish to change this value then you
should use the function
[gc_target_frame_time()](gc_target_frame_time) .

#### Syntax:

``` gml
gc_get_target_frame_time(time);
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if (gc_get_target_frame_time() != 50)
{
    gc_target_frame_time(50);
}
```

The above code checks the current frame time target for the garbage
collector and if it is not 50 microseconds then it is set to this value.
