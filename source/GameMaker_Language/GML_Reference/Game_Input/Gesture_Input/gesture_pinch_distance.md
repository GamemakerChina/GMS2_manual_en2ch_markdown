# gesture_pinch_distance

This function is used to set the distance within which you have to
touch/click the screen and move with two fingers before you trigger a
[Pinch
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
. The distance is measured in inches and has a default value of 0.1.

#### **Syntax:**

``` gml
gesture_pinch_distance();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_pinch_distance() != 0.1
{
    gesture_pinch_distance(0.1);
}
```

The above code checks to see if the pinch distance for gestures is set
to 0.1 inches and if it is not it sets it to that value.
