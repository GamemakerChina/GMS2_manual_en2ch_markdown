# keyboard_check_direct

This function will return true if the key with the particular keycode is
pressed, or false if it is not, by checking the hardware directly. It
allows for a few more checks, in particular you can use keycodes
**vk_lshift** , **vk_lcontrol** , **vk_lalt** , **vk_rshift** ,
**vk_rcontrol** and **vk_ralt** to check whether the left or right
shift, control or alt key is pressed. The function will take a keycode
value as returned by the function [ ord() ](../../Strings/ord) (only
*capital* letters from A-Z or numbers from 0-9), or any of the vk\_\*
constants listed on the main [Keyboard Input](Keyboard_Input) page.
** NOTE ** This function is only available for the standard Windows
target and the result is independent of which application has focus.

#### **Syntax:**

``` gml
keyboard_check_direct(key);
```

|          |                                                                                                                                 |                                     |
|----------|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| Argument | Type                                                                                                                            | Description                         |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | The key to check the down state of. |

#### **Returns:**

``` gml
 Boolean
```

#### **Example:**

``` gml
if keyboard_check_direct(vk_ralt) || keyboard_check_direct(vk_lalt)
{
    crouch = true;
}
```

The above code will check to see if either the left or right alt keys
have been pressed, and if they have it sets the variable "crouch" to
true.
