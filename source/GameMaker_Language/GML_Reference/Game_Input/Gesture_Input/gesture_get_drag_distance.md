# gesture_get_drag_distance

This function is used to get the distance it takes for a [Dragging
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
event to be triggered by the movement of a touch or click. The distance
is measured in inches and has a default value of 0.1.

#### **Syntax:**

``` gml
gesture_get_drag_distance();
```

#### Returns:

``` gml
 Real

(inches)
```

#### Example:

``` gml
if gesture_get_drag_distance() != 0.1
{
    gesture_drag_distance(0.1);
}
```

The above code checks to see if the drag distance for gestures is set to
0.1 inches and if it is not it sets it to that value.
