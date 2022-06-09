# gesture_get_rotate_time

This function is used to get the angle which a pair of touches must
exceed in order to trigger a [Rotate Start
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
. The angle is measured in degrees and has a default value of 5°.

#### **Syntax:**

``` gml
gesture_get_rotate_angle();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_rotate_angle() != 5
{
    gesture_rotate_angle(5);
}
```

The above code checks to see if rotation angle for gestures is set to 5°
and if it is not it sets it to that value.
