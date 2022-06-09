# view_enabled

This variable controls whether any view ports that are visible within
the room are enabled or not. If you have view ports set to visible and
then disable this option, the whole room will be drawn to the screen
scaled to the window size instead of the different cameras being drawn
through the view ports.

#### Syntax:

``` gml
view_enabled;
```

#### Returns:

``` gml
 Boolean

(true: enabled, false: disabled)
```

#### Example:

``` gml
if !view_enabled
{
    view_visible[0] = true;
    view_enabled = true;
}
```

The above code checks to see if views are enabled for the room, and if
they are not, it makes sure that view port\[0\] is visible and then
enables views for the room.
