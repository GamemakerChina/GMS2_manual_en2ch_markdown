# gpu_get_colourwriteenable

This function can be used to retrieve the current colour write-enable
values. The function returns a 4 element 1D array with the following
elements in it which will be either true (enabled) or false (disabled).
By default all colour writing is set to true :

-   \[0\] = Red channel enabled/disabled
-   \[1\] = Green channel enabled/disabled
-   \[2\] = Blue channel enabled/disabled
-   \[3\] = Alpha channel enabled/disabled

#### Syntax:

``` gml
gpu_get_colorwriteenable();
```

#### Returns:

``` gml
 Array

(4 elements only; see above for details)
```

#### Example:

``` gml
var cw = gpu_get_colorwriteenable();
cw[3] = false;
gpu_set_colorwriteenable(cw);
```

The above code gets the current colour write values and then sets the
alpha component to false .
