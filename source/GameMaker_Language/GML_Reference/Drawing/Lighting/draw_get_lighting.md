# draw_get_lighting

This function will return whether lighting is enabled ( true ) or not (
false ) for the whole scene.

#### Syntax:

``` gml
draw_get_lighting()
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !draw_get_lighting()
{
    draw_set_lighting(true);
}
```

The above code will check to see if lighting is enabled for the scene,
and if not it enables it.
