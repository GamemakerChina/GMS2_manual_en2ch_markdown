# gesture_pinch_angle_towards

This function is used to set the angle within which a touch must be
moving towards another touch before a [Pinch In
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
may potentially be started. The angle is measured in degrees and has a
default value of 45°.

#### **Syntax:**

``` gml
gesture_pinch_angle_towards();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_pinch_angle_towards() != 45
{
    gesture_pinch_angle_towards(45);
}
```

The above code checks to see if the pinch in angle for gestures is set
to 45° and if it is not it sets it to that value.
