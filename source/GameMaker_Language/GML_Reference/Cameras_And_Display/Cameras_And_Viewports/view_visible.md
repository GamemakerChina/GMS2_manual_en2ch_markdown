# view_visible

This variable can be used to find out if a particular view port is
currently visible or not. You can also set this variable to effectively
turn "on" or "off" a view by setting the value to true (visible) or
false (invisible). Note that even if you have a view port set to
visible, if view ports are not enabled (using the built-in variable [
view_enabled ](view_enabled) or enabling them in the Room Editor)
then they will not be drawn to the screen.

#### Syntax:

``` gml
view_visible[0 ... 7];
```

#### Returns:

``` gml
 Boolean

(true: enabled, false: disabled)
```

#### Example:

``` gml
if !view_visible[0]
{
    view_visible[0] = true;
}
```

The above code checks to see if view\[0\] is visible or not and if it is
not, it then sets it to be visible.
