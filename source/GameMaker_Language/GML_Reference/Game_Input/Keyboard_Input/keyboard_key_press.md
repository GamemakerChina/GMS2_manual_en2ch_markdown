# keyboard_key_press

With this function you can simulate the press of any key on the
keyboard. When used, the key will be flagged as being pressed until the
corresponding release function is called (see [ keyboard_key_release()
](keyboard_key_release) ). The function will take a keycode value as
returned by the function [ ord() ](../../Strings/ord) (only
*capital* letters from A-Z or numbers from 0-9), or any of the vk\_\*
constants listed on the main [Keyboard Input](Keyboard_Input) page.
Note that after calling this function, if the key is *physically*
pressed on the keyboard, this press event will *not* be registered again
until the key has been physically released (triggering the release event
and stopping this function), or the corresponding release key function
has been called, and the key pressed again.

#### **Syntax:**

``` gml
keyboard_key_press(key);
```

|          |                                                                                                                                 |                                 |
|----------|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------|
| Argument | Type                                                                                                                            | Description                     |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | The key to simulate a press of. |

#### **Returns:**

``` gml
N/A
```

#### **Example:**

``` gml
keyboard_key_press(vk_space);
```

This will simulate a spacebar press.
