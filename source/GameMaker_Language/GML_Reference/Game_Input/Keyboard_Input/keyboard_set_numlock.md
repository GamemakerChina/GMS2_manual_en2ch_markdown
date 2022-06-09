# keyboard_set_numlock

You can use this function to switch the keypad number-lock on or off
(set to **true** for on, and **false** for off). ** NOTE ** This
functionality is only available in the Windows target builds and will
not function on any other device.

#### **Syntax:**

``` gml
keyboard_set_numlock(value);
```

|          |                                                                            |                                               |
|----------|----------------------------------------------------------------------------|-----------------------------------------------|
| Argument | Type                                                                       | Description                                   |
| value    |  [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)  | Set this to true for "on" and false for "off" |

#### **Returns:**

``` gml
N/A
```

#### **Example:**

``` gml
if keyboard_get_numlock()
{
    keyboard_set_numlock(false);
}
else
{
    keyboard_set_numlock(true);
}
```

The above example code will get the state of the numberlock key and if
it is on (true) it will set it to off (false) and vice-versa.
