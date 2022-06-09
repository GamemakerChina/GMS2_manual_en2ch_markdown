# begin / end

The GameMaker Language permits you to use the keywords begin and end
instead of the more usual curly brackets {} when creating code blocks.
The code example below shows how this works:

``` gml
if (!visible)     begin
     exit;
     end
 while (place_meeting(x, y))     begin
     x -= lengthdir_x(1, direction - 180);     y -= lengthdir_y(1, direction - 180);     end
```

Note that using these keywords is not typical and is provided as part of
the language more for legacy support than for anything else, and at any
time in the future they may be deprecated.
