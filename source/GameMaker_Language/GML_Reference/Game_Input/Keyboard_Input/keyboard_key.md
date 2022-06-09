# keyboard_key

With this variable you can get the keycode of the key that is currently
being pressed and it will return 0 if no key is being pressed when the
check is done.

#### **Syntax:**

``` gml
keyboard_key;
```

#### **Returns:**

``` gml
 Virtual Key Constant (vk_*)
```

#### **Example:**

``` gml
switch (keyboard_key)
{
    case vk_numpad1: gun = weapon[0][0]; break;
    case vk_numpad2: gun = weapon[1][0]; break;
    case vk_numpad3: gun = weapon[2][0]; break;
}
```

The above code uses the value of the keyboard_key variable to set a
variable to the same value as an array.
