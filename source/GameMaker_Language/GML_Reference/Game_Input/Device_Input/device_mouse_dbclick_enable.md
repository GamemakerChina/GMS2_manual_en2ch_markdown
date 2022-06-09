# device_mouse_dbclick_enable

This function can be used to set the device to detect a double tap of
the mb_left (left mouse button) as an mb_right (right mouse button)
input. By default this is set to true , meaning that every time the user
taps the device screen twice quickly and consecutively, the return value
is the same as if the right mouse button had been clicked. When this is
on, the first tap will be detected as mb_left , and the second as
mb_right , so make sure that any code you use takes this into account.

#### Syntax:

``` gml
device_mouse_dbclick_enable(bool);
```

|          |                                                                            |                                                              |
|----------|----------------------------------------------------------------------------|--------------------------------------------------------------|
| Argument | Type                                                                       | Description                                                  |
| bool     |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Set double-click detection on ( true ) or off ( false ).     |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if os_type == os_windows || os_type == os_mac
{
    device_mouse_dbclick_enable(false);
}
```

The above code checks to see if the device running the game is a Windows
PC or a Mac and if it is either of them, it disables the double tap
function.
