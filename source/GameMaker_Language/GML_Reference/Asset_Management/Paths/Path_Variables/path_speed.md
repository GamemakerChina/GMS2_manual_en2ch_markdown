# path_speed

You can use this function to get or to set the speed of a path after it
has been started using the function [path_start()](../path_start) .
You can use negative values to signify that the instance should follow
the path in reverse.

#### Syntax:

``` gml
path_speed;
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
path_speed = -1 + random(2);
```

The above code will set the instance to travel the path at a random
speed between -1 and 1.
