# gesture_get_double_tap_distance

This function is used to get the distance within which you have to
touch/click the screen again after a single tap in order to trigger a
[Double Tap
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
. The distance is measured in inches and has a default value of 0.1.

#### **Syntax:**

``` gml
gesture_get_double_tap_distance();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_double_tap_distance() != 0.1
{
    gesture_double_tap_distance(0.1);
}
```

The above code checks to see if double tap distance for gestures is set
to 0.1 inches and if it is not it sets it to that value.
