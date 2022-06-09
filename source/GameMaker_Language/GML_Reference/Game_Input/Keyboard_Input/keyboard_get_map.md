# keyboard_get_map

Sometimes you may wish to get the ascii code for a mapped key (to see if
it is already mapped, for example) which is what this function
returns. The function will take a keycode value as returned by the
function [ ord() ](../../Strings/ord) (only *capital* letters from
A-Z or numbers from 0-9), or any of the vk\_\* constants listed on the
main [Keyboard Input](Keyboard_Input) page.

#### **Syntax:**

``` gml
keyboard_get_map(key);
```

|          |                                                                                                                                 |                                                            |
|----------|---------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| Argument | Type                                                                                                                            | Description                                                |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | This is the key that you wish to get the mapped value from |

#### **Returns:**

``` gml
 Real
```

#### **Example:**

``` gml
if keyboard_get_map(ord("A")) = ord("A")
{
    keyboard_set_map(ord("A"), keyboard_lastkey);
}
```

The above example code will first check and see if "A" has been mapped
to another key, and if it hasn't it will map it to the last key that the
user has pressed.
