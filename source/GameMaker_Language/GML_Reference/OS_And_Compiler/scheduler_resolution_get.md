# scheduler_resolution_get

This function is used to retrieve the resolution of the Windows thread
scheduler in milliseconds. If the scheduler's resolution is set to the
default value (as set by Windows), the function will return -1. For
information on the thread scheduler, see the page for
[scheduler_resolution_set()](scheduler_resolution_set) . **NOTE** :
This function is for **Windows** only.

#### Syntax:

``` gml
scheduler_resolution_get();
```

#### Returns:

``` gml
 Real

(or -1 for default)
```

#### Example:

``` gml
scheduler_resolution = scheduler_resolution_get();
```

This example retrieves the resolution of the Windows thread scheduler,
and stores it in the " scheduler_resolution" variable.
