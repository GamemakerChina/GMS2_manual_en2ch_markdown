# path_end

Calling this function will end the current path that the instance is
following, as set when the function [ path_start() ](path_start) was
called..

#### Syntax:

``` gml
path_end();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if place_meeting(x, y, obj_Blocker)
{
    path_end();
}
```

The above code will end the current path if the instance detects any
collision with any instance of the given object.
