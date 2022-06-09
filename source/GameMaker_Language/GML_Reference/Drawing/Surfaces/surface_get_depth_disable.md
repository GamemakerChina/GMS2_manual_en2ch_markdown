# surface_get_depth_disable

This function checks to see if the automatic depth buffer generation for
surfaces is enabled. Normally all surfaces have depth buffers so if you
draw 3D objects to them then it'll sort them properly by depth, however
allocating depth buffers essentially doubles the size of surfaces, which
could be an excessive and unnecessary overhead especially if your game
is very memory intensive or predominantly 2D. In these cases you can
check this using this function and disable the depth buffer for surfaces
if required using the function [ surface_depth_disable()
](surface_depth_disable) .

#### Syntax:

``` gml
surface_get_depth_disable();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (!surface_exists(surf))
{
    if surface_get_depth_disable() == false
    {
        surface_depth_disable(true);
    }
    surf = surface_create(room_width, room_height);
}
```

The above code will check to see if the given surface exists, and if it
does not, then it checks the current state of the surface depth buffer
and if it is enabled, it will disable it instead, before finally
creating the surface.
