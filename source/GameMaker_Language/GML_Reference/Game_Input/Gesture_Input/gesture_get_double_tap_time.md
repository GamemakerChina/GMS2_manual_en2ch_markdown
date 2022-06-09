# gesture_get_double_tap_time

This function is used to get the time it takes between two
touches/clicks to trigger a [Double Tap
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
event. The time is measured in seconds and has a default value of 0.10.

#### **Syntax:**

``` gml
gesture_get_double_tap_time();
```

#### Returns:

``` gml
 Real

(seconds)
```

#### Example:

``` gml
if gesture_get_double_tap_time() != 0.16
{
    gesture_double_tap_time(0.16);
}
```

The above code checks to see if double tap time for gestures is set to
0.16 seconds and if it is not, it sets it to that value.
