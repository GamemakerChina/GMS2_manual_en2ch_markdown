# keyboard_virtual_height

This function will return the current height in pixels of the virtual
keyboard, based on the size of the *display* . If the keyboard is not
visible, 0 will be returned.

#### Syntax

``` gml
keyboard_virtual_height();
```

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if keyboard_virtual_status() == true
{
    key_h = keyboard_virtual_height();
}
```

The above code will check the status of the OS virtual keyboard, and if
it's visible set a variable to the height of the keyboard.
