# keyboard_check

With this function you can check to see if a key is held down or not.
Unlike the [ keyboard_check_pressed() ](keyboard_check_pressed) or [
keyboard_check_released() ](keyboard_check_released) functions which
are only triggered once when the key is pressed or released, this
function is triggered every step that the key is held down for. The
function will take a keycode value as returned by the function [ ord()
](../../Strings/ord) (only *capital* letters from A-Z or numbers
from 0-9), or any of the vk\_\* constants listed on the main [Keyboard
Input](Keyboard_Input) page.

#### **Syntax:**

``` gml
keyboard_check(key);
```

|          |                                                                                                                                 |                                     |
|----------|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                                            | Description                         |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | The key to check the down state of. |

#### **Returns:**

``` gml
 Boolean
```

#### ****Example:****

``` gml
if keyboard_check(vk_left)
{
    x -= 5;
}
```

The above code will check to see if the arrow key is being pressed and
move the instance 5 pixels left every step that it returns true.
