# gpu_get_alphatestenable

With this function you can check to see whether alpha testing is enabled
(returns true ) or not (returns false ). For more information on alpha
testing, see the function [ gpu_set_alphatestref()
](gpu_set_alphatestref) .

#### Syntax:

``` gml
gpu_get_alphatestenable();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if !gpu_get_alphatestenable()
{
    gpu_set_alphatestenable(true);
    gpu_set_alphatestref(128);
}
```

The above code will check to see if alpha testing is enabled and if not
it will switch on alpha testing and set the test threshold to 128 (only
pixels with an alpha over 0.5 will be drawn).
