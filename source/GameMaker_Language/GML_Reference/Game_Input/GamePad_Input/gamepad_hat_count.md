# gamepad_hat_count

This function will return the *total* number of hats available for the
gamepad connected to the given device "slot". Hats generally refer to
up/down/left/right buttons, and note that on the Windows target, hats
are only available on DirectInput controllers (so, from slot 4 upwards).

#### Syntax:

``` gml
gamepad_hat_count(device);
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
h_num = gamepad_hat_count(4);
```

The above code will return the number of hats available on the gamepad
plugged into device "slot" 4 and store the value in the variable
"h_num".
