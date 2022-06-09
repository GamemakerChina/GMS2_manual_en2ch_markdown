# timeline_loop

This variable will return whether the time line is looping (true) or not
(false). You can change this variable to switch looping on or off and it
works with a negative time line speed (if the time line position goes
below 0 it will start again at the last defined moment).

#### Syntax:

``` gml
timeline_loop;
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !timeline_loop
{
    timeline_loop = true;
}
```

The above code checks to see of the time line currently assigned to an
instance will loop or not and if it doesn't it sets it to true.
