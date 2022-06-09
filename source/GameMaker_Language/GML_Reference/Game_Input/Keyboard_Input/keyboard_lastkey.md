# keyboard_lastkey

This variable refers to the value that [ keyboard_key
](keyboard_key) was in the previous frame, returning the keycode of
that key (all standard keycode constants are returned). This variable is
*not* read only and you can change it, for example to set it to -1 if
you handled it already.

#### **Syntax:**

``` gml
keyboard_lastkey;
```

#### **Returns:**

``` gml
 Virtual Key Constant (vk_*)
```

#### **Example:**

``` gml
if (keyboard_lastkey != -1)
{
    str += keyboard_lastchar;
    keyboard_lastkey = -1;
}
```

The above code checks to see if the lastkey variable is not equal to -1,
and if it is it adds whatever the last key was as a string to the
variable "str", then it resets the keyboard_lastkey variable to accept
further input.
