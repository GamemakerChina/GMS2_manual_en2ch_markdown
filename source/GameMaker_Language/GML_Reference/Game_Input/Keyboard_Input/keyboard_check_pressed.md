# keyboard_check_pressed

With this function you can check to see if a key has been pressed or
not. Unlike the [ keyboard_check() ](keyboard_check) function, this
function will only run once for every time the key is pressed down, so
for it to trigger again, the key must be first released and then pressed
again. The function will take a keycode value as returned by the
function [ ord() ](../../Strings/ord) (only *capital* letters from
A-Z or numbers from 0-9), or any of the vk\_\* constants listed on the
main [Keyboard Input](Keyboard_Input) page.

#### **Syntax:**

``` gml
keyboard_check_pressed(key);
```

|          |                                                                                                                                 |                                        |
|----------|---------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Argument | Type                                                                                                                            | Description                            |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | The key to check the pressed state of. |

#### **Returns:**

``` gml
 Boolean
```

#### **Example:**

``` gml
if keyboard_check_pressed(vk_anykey)
{
    room_goto_next();
}
```

The above code will advance to the next room if the player presses any
of the keyboard's keys (working like a "Press Any Key to
Continue" prompt).
