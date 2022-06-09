# keyboard_virtual_status

This function can be used to get the status of the virtual keyboard on
the device running the game. The function will return true if the OS
virtual keyboard is visible/being shown or false if it is hidden/hiding.

#### Syntax

``` gml
keyboard_virtual_status();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
var _status = keyboard_virtual_status();
if _status == false
{
    keyboard_virtual_show(kbv_type_numbers, kbv_returnkey_default, kbv_autocapitalize_none, false);
}
```

The above code will show the OS virtual keyboard if the current status
is false .
