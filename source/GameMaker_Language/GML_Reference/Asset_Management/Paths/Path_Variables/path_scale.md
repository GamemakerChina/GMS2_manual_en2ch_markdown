# path_scale

This value can be used to get or to set the scale of the currently
assigned path for the instance (as set by the function
[path_start()](../path_start) ) with a default value of 1. This is a
scalar value, so 1 is a scale of 1:1, while setting it to 2, for
example, will be double the scale and setting it to 0.5 would be halving
the scale.

#### Syntax:

``` gml
path_scale;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
path_scale = 1 + random(2);
```

The above code will set the current path's scale to a random size
between 1 (its original size) and 3 (3 times its original size).
