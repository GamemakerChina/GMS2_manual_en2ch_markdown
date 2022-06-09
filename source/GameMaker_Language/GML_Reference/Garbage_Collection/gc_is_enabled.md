# gc_is_enabled

With this function you can check to see if the garbage collector is
enabled or not. The function will return true if it is enabled or false
otherwise.

#### Syntax:

``` gml
gc_is_enabled();
```

#### Returns:

``` gml
 Boolean
```

#### Example:

``` gml
if (!gc_is_enabled())
{
    gc_enable(true);
}
```

The above code checks to see if the garbage collector is enabled and if
it isn't it enables it.
