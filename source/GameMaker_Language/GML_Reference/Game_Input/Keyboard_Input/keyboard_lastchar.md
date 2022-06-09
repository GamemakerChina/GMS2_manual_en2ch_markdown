# keyboard_lastchar

This variable stores a string of the last key pressed. This variable is
*not* read only and you can change it, for example to set it to "" (an
empty string) if you handled it already.

#### **Syntax:**

``` gml
keyboard_lastchar;
```

#### **Returns:**

``` gml
 String
```

#### **Example:**

``` gml
if keyboard_lastkey != -1
{
    str += keyboard_lastchar;
    keyboard_lastkey = -1;
}
```

The above code checks to see if the lastkey variable is greater than -1,
and if it is it adds whatever the last key was as a string to the
variable "str".
