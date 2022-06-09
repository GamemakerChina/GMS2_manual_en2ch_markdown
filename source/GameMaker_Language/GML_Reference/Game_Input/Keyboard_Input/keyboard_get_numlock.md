# keyboard_get_numlock

You can use this function to find the status of the keypad number lock
with **true** being returned for on, and **false** returned for off. **
NOTE ** This functionality is only available in the Windows exe builds
and will not function on any other device.

#### **Syntax:**

``` gml
keyboard_get_numlock();
```

#### **Returns:**

``` gml
 Boolean
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
