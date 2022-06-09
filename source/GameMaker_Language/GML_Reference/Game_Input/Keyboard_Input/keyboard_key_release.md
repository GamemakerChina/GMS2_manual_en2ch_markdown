# keyboard_key_release

With this function you can simulate the release of any key on the
keyboard. The function will take a keycode value as returned by the
function [ ord() ](../../Strings/ord) (only *capital* letters from
A-Z or numbers from 0-9), or any of the vk\_\* constants listed on the
main [Keyboard Input](Keyboard_Input) page.

#### **Syntax:**

``` gml
keyboard_key_release(key);
```

|          |                                                                                                                                 |                                   |
|----------|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| Argument | Type                                                                                                                            | Description                       |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | The key to simulate a release of. |

#### **Returns:**

``` gml
N/A
```

#### **Example:**

``` gml
keyboard_key_release(vk_space);
```

This will simulate a spacebar release.
