# device_mouse_x

This function returns the x position of a touch on the device. If you
are running this on a the HTML5 or PC and Mac modules then this value is
updated constantly, as long as the device (usually a mouse) is plugged
in, however for mobile devices, this will only be updated while the
screen is being touched and note that the maximum number of touches that
can be detected will depend very much on the device being used and the
OS it runs.

#### Syntax:

``` gml
device_mouse_x(device);
```

|          |                                                                         |                                                   |
|----------|-------------------------------------------------------------------------|---------------------------------------------------|
| Argument | Type                                                                    | Description                                       |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The device (from 0 - *n* ) that is being checked. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
if device_mouse_check_button(0, mb_left)
{
    if device_mouse_x(0) &amp;gt; x-32 &amp;amp;&amp;amp; device_mouse_x(0) &amp;lt; x+32
    {
        pressed = true;
    }
    else
    {
        pressed = false;
    }
}
```

The above code checks to see if the device is being pressed and if so it
then polls the device x position to see if it is within the parameters.
If it is it sets the variable "pressed" to true , other wise it sets it
to false .
