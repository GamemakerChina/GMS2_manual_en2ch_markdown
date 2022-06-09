# gpu_get_zwriteenable

This function can be used to retrieve whether z-writing is enabled (the
function returns true ) or not (the function returns false ). The
default value is that z-writing is *enabled* , so the function will
return true .

#### Syntax:

``` gml
gpu_get_zwriteenable();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gpu_get_zwriteenable() == false
{
    gpu_set_zwriteenable(true);
}
```

The above code checks to see if z-writing is enabled or not and if it is
disabled it is then enabled again.
