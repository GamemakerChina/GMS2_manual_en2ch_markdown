# gamepad_axis_count

This function will return the number of "axis" controls on the device
being checked. These controls are the analogue direction "thumbsticks"
on most controllers.

#### Syntax:

``` gml
gamepad_axis_count(device);
```

|          |                                                                         |                                       |
|----------|-------------------------------------------------------------------------|---------------------------------------|
| Argument | Type                                                                    | Description                           |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad device "slot" to check. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
axis = gamepad_axis_count(0))
```

The above code stores the number of axes available for the gamepad
connected to device "slot" 0 in the variable "axis".
