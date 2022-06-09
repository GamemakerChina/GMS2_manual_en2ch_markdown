# gamepad_remove_mapping

This function can be used to remove the current device mapping from the
given gamepad slot index. Once called, the slot index will need to be
remapped using the [ gamepad_test_mapping() ](gamepad_test_mapping)
function if you want to be able to be able to use the gamepad constants
to detect input correctly (direct input can always be retrieved using
the [gamepad_axis](gamepad_axis_count) /
[button](gamepad_button_count) /
[hat_count()](gamepad_hat_count) and
[gamepad_axis](gamepad_axis_value) /
[button](gamepad_button_value) /
[hat_value()](gamepad_hat_value) functions together).

#### Syntax:

``` gml
gamepad_remove_mapping(index);
```

|          |                                                                         |                                                        |
|----------|-------------------------------------------------------------------------|--------------------------------------------------------|
| Argument | Type                                                                    | Description                                            |
| index    |  [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Which gamepad index "slot" to remove the mapping from. |

#### Returns:

``` gml
N/A
```

#### Example:

``` gml
if remap == true
{
    gamepad_remove_mapping(global.PadIndex);
}
```

The above code will remove the mapping from the given gamepad index slot
based on the value of a variable.
