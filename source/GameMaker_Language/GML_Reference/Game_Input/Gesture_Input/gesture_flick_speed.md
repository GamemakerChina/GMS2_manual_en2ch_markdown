# gesture_flick_speed

This function is used to set the speed required for a [Flick
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
event to be triggered when a touch or click is released. The speed is
measured in inches per second and has a default value of 2.0.

#### **Syntax:**

``` gml
gesture_flick_speed(speed);
```

|          |                                                                         |                                                                            |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                                |
| speed    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The speed (in inches per second) to set for flick gesture event detection. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if gesture_get_flick_speed() != 2
{
    gesture_flick_speed(2);
}
```

The above code checks to see if the flick speed for gestures is set to 2
inches per second and if it is not it sets it to that value.
