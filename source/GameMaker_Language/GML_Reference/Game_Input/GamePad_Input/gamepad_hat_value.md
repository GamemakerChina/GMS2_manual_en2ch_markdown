# gamepad_hat_value

With this function you can get the current value of a gamepad "hat".
Each hat value is a bit-mask for the different directions where:

-   Up = 1
-   Right = 2
-   Down = 4
-   Left = 8

Note that these can be combined (for example, supplying a hat index of 3
would be checking up and right, or you can use the \| operator to
combine the various values) but only at most 2 bits can be pressed at
once. The function will return a real value between 0 and 1, where 0 is
not pressed and 1 is fully pressed (and there may be values in between
depending on whether the gamepad supports analog input for hats).

#### Syntax:

``` gml
gamepad_hat_value(device, hatindex);
```

|          |                                                                         |                                           |
|----------|-------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                    | Description                               |
| device   |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad device "slot" to check.     |
| hatindex |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad hat (or hats) to check for. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
var _dir = gamepad_hat_value(global.PadIndex, 0);
switch (_dir)
{
    case 1: y -= 3; break;
    case 2: x += 3; break;
    case 3: y -= 3; x += 3; break;
    case 4: x -= 3; break;
    case 6: y += 3; x += 3; break;
    case 8: y += 3; break;
    case 9: y -= 3; x -= 3; break;
    case 12: y += 3; x -= 3; break;
}
```

The above code stores the state of the hat "0" in a local variable, then
checks to see what the return value is and acts accordingly.
