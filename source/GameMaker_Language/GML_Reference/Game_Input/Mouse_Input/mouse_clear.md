# mouse_clear

This function will clear the current state of the given mouse button.
This means that checks for it being held down will not return true until
the player releases the button and presses it again (but the release
state will still be detected if the clear is done while the mouse button
is being held down). You can supply one of the mouse button
constants listed [on this page](Mouse_Input) .

#### Syntax:

``` gml
mouse_clear(button);
```

|          |                                                                                                                          |                                           |
|----------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| Argument | Type                                                                                                                     | Description                               |
| button   |  [Mouse Button Constant](../../../../../GameMaker_Language/GML_Reference/Game_Input/Mouse_Input/mouse_check_button)  | Which mouse button constant to check for. |

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
mouse_clear(mb_any);
```

The above code will clear the down state of all the mouse buttons.
