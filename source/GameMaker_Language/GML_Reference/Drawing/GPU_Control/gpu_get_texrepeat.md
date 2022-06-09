# gpu_get_texrepeat

With this function you can check to see whether texture repeating is
enabled (returns true ) or not (returns false ). For more information on
texture repeating, see the function [ gpu_set_texrepeat()
](gpu_set_texrepeat) .

#### Syntax:

``` gml
gpu_get_texrepeat();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if gpu_get_texrepeat()
{
    gpu_set_texrepeat(false);
}
else
{
    gpu_set_texrepeat(true);
}
```

The above code checks to see if texture repeating is on or off and
switches it accordingly.
