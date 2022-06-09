# gesture_rotate_time

This function is used to set the time within which a pair of touches
must be rotating in a consistent direction for a [Rotate Start
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
to be triggered. The time is measured in seconds and has a default value
of 0.16s. **IMPORTANT!** Currently for a 60fps game you can only set
this to a maximum of one second otherwise no rotations will be detected.
This will increase for a lower framrate, for example a 30fps game can
have a maximum time of 2 seconds.

#### **Syntax:**

``` gml
gesture_rotate_time();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_rotate_time() != 0.1
{
    gesture_rotate_time(0.1);
}
```

The above code checks to see if the rotate time for gestures is set to
0.1 seconds and if it is not it sets it to that value.
