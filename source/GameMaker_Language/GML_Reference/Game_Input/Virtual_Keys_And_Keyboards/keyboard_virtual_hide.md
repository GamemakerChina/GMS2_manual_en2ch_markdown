# keyboard_virtual_hide

This function can be used to hide the virtual keyboard on the device
running the game. Calling this function will generate a [System
Asynchronous
Event](../../../../The_Asset_Editors/Object_Properties/Async_Events/System)
, in which the async_load DS map will be populated with the following
key/value pairs:

-   " **event_type** " - this will be " **virtual keyboard status** "
    when triggered by virtual keyboard functions.
-   " **screen_height** " - the height of the virtual keyboard (in
    pixels). This will be 0 if the keyboard is invisible.
-   " **keyboard_status** " - the current status of the keyboard,
    returned as one of the following strings:
    -   "hiding"
    -   "hidden"
    -   "showing"
    -   "visible"

#### Syntax

``` gml
keyboard_virtual_hide();
```

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if input == true
{
    input = false;
    keyboard_virtual_hide();
}
```

The above code will hide the OS virtual keyboard if the given variable
is not set to false .
