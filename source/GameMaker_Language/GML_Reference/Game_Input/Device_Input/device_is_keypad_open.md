# device_is_keypad_open

This does a check of the device for a keypad and if one is available it
returns true otherwise it returns false . Please note that this function
is mainly for use with Android devices For those users with a *Sony
Xperia Play* , there is a set button/key map setup within GameMaker , so
you can use the [keyboard
constants](../Keyboard_Input/Keyboard_Input) **vk_up** , **vk_down**
, **vk_left** , **vk_right** for the joypad keys and *Triangle* is
ord("T") , *Square* is ord("S") , *Circle* is **vk_alt** +
**vk_backspace** while the *back* button is simply vk_backspace ,
*Cross* is **vk_space** , *Select* is **vk_return** and *Start* is
**vk_rshift** , the *L Trigger* is ord("L") and *R Trigger* is ord("R")
.

#### Syntax:

``` gml
device_is_keypad_open
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if device_is_keypad_open()
{
     global.Setting = 2;
}
else
{
     global.Setting = 1;
}
```

The above code checks for a keypad then changes a global variable
depending on the returned value.
