# gamepad_button_count

This function will return the *total* number of buttons available for
the gamepad connected to the given device "slot".

#### Syntax:

``` gml
gamepad_button_count(device);
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
b_num = gamepad_button_count(0);
```

The above code will return the number of buttons available on the
gamepad plugged into device "slot" 0 and store the value in the variable
"b_num".
