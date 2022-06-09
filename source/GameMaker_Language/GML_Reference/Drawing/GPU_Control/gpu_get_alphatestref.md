# gpu_get_alphatestref

You can use this function to find the current value for the alpha test
reference (default is 0, but you can use [ gpu_set_alphatestref()
](gpu_set_alphatestref) to set this value to something other than
this).

#### Syntax:

``` gml
gpu_get_alphatestref();
```

#### Returns:

``` gml
 Real

(from 0 - 255)
```

#### Example:

``` gml
if gpu_get_alphatestenable()
{
    if gpu_get_alphatestref() &amp;lt; 254
    {
        gpu_set_alphatestref(254);
    }
}
```

The above code checks to see if alpha testing is enabled, and if it is,
it then checks the current alpha test reference value and sets it if it
is less than 254.
