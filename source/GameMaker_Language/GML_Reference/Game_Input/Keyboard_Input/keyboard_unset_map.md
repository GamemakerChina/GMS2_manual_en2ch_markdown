# keyboard_unset_map

With this function you can clear all re-mapped keys so that they return
to their default state, ie: all keys to map to themselves.

#### **Syntax:**

``` gml
keyboard_get_map();
```

#### **Returns:**

``` gml
N/A
```

#### **Example:**

``` gml
if keyboard_check_pressed(vk_escape)
{
    keyboard_unset_map();
}
```

The above example code will reset all mapped keys to their default
settings if the user presses the "escape" key.
