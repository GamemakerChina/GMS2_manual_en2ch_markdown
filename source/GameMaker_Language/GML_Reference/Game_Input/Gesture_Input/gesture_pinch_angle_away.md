# gesture_pinch_angle_away

This function is used to set the angle within which a touch must be
moving away from another touch before a [Pinch Out
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
may potentially be started. The angle is measured in degrees and has a
default value of 45°.

#### **Syntax:**

``` gml
gesture_pinch_angle_away();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_pinch_angle_away() != 45
{
    gesture_pinch_angle_away(45);
}
```

The above code checks to see if the pinch out angle for gestures is set
to 45° and if it is not it sets it to that value
