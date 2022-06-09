# gesture_drag_time

This function is used to set the time it takes for a [Drag
Gesture](../../../../The_Asset_Editors/Object_Properties/Gesture_Events)
event to be triggered by a touch or click. This time will also affect
how the **Tap Event** is triggered as a touch/click and release before
this time is up will be considered a Tap. The time is measured in
seconds and has a default value of 0.16.

#### **Syntax:**

``` gml
gesture_drag_time(time);
```

|          |                                                                         |                                                                |
|----------|-------------------------------------------------------------------------|----------------------------------------------------------------|
| Argument | Type                                                                    | Description                                                    |
| time     |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | The time (in seconds) to set for drag gesture event detection. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if gesture_get_drag_time() != 0.16
{
    gesture_drag_time(0.16);
}
```

The above code checks to see if drag time for gestures is set to 0.16
seconds and if it is not it sets it to that value.
