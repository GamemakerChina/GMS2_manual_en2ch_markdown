# keyboard_check_released

With this function you can check to see if a key has been released or
not. Unlike the [ keyboard_check() ](keyboard_check) function, this
function will only run once for every time the key is lifted, so for it
to trigger again, the key must be first pressed and then released again.
The function will take a keycode value as returned by the function [
ord() ](../../Strings/ord) (only *capital* letters from A-Z or
numbers from 0-9), or any of the vk\_\* constants listed on the main
[Keyboard Input](Keyboard_Input) page.

#### **Syntax:**

``` gml
keyboard_check_released(key);
```

|          |                                                                                                                                 |                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| Argument | Type                                                                                                                            | Description                             |
| key      |  [Virtual Key Constant (vk\_\*)](../../../../../GameMaker_Language/GML_Reference/Game_Input/Keyboard_Input/Keyboard_Input)  | The key to check the released state of. |

#### **Returns:**

``` gml
 Boolean
```

#### **Example:**

``` gml
if keyboard_check_released(ord("P"))
{
    instance_create_layer(0, 0, "Controllers", obj_Pause);
}
```

The above code will check to see if the "P" key has been released and if
so, create an instance of "obj_Pause".
