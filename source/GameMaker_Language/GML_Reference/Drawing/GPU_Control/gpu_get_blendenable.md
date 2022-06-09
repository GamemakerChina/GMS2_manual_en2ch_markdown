# gpu_get_blendenable

This function can be used to retrieve the alpha-blending state. If it
returns true then alpha-blending is enabled, and if it returns false it
is disabled. By default this is on and so the function will return true

#### Syntax:

``` gml
gpu_get_blendenable();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gpu_get_blendenable() == false
{
    gpu_set_blendenable(true);
}
```

The above code checks the state of the alpha blending and if it is
disabled it is then enabled again.
