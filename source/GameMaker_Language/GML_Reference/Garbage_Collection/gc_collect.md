# gc_collect

With this function you can trigger the garbage collector, forcing it to
run at the end of the current frame (step). It is worth noting that the
garbage collector does *not* need to be active for this to work. Calling
this function after disabling the garbage collector (using the function
[gc_enable()](gc_enable) ) will enable the garbage collector for one
frame in which all objects that have been flagged for collection will be
removed from memory before the garbage collector is disabled again.

#### Syntax:

``` gml
gc_collect();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if (global.debug == true &amp;amp;&amp;amp; keyboard_check_pressed(vk_f1))
{
    gc_collect();
}
```

The above code checks a global variable and a key being pressed and if
those are true then garbage collection is triggered for the end of the
frame (step).
