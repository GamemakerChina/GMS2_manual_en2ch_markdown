# display_get_orientation

This function will return one of four constants GameMaker has to tell
you whether the device running the game is being held in landscape or
portrait mode (see the table below). Note that this function may not
correctly detect the orientation of the device when used in the HTML5
target module. However this is easily mimicked by the use of the
following script:

``` gml
return (browser_width &amp;lt; browser_height);
```

Such a function would return true for portrait and false for landscape.

#### Syntax:

``` gml
display_get_orientation()
```

#### Returns:

``` gml
 Display Orientation Constant
```

|                                                                                                                                |                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
|  [Display Orientation Constant](../../../../GameMaker_Language/GML_Reference/Cameras_And_Display/display_get_orientation)  |                                                                                                                        |
| Constant                                                                                                                       | Description                                                                                                            |
|  display_landscape                                                                                                             | The device is being held horizontally ie: The longest edge is from left to right, and the menu button is on the right. |
|  display_landscape_flipped                                                                                                     | As above, only now the menu button is on the left.                                                                     |
|  display_portrait                                                                                                              | The device is being held vertically ie: The longest edge is from top to bottom, and the menu button is at the bottom.  |
|  display_portrait_flipped                                                                                                      | As above, only now the menu button is at the top.                                                                      |

#### Example:

``` gml
if display_get_orientation() == display_landscape
{
    global.Config = 0;
}
else
{
    global.Config = 1;
}
```

The above code checks the orientation of the device and sets a global
variable depending on the value returned.
