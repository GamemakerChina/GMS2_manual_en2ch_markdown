# gpu_get_ztestenable

This function can be used to retrieve whether z-testing is enabled (the
function returns true ) or not (the function returns false ). The
default value is that z-testing is *disabled* , so the function will
return false .

#### Syntax:

``` gml
gpu_get_ztestenable();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gpu_get_ztestenable() == false
{
    gpu_set_ztestenable(true);
}
```

The above code checks to see if z-testing is enabled or not and if it is
disabled it is then enabled again.
