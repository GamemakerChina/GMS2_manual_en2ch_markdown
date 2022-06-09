# gpu_get_fog

This function can be used to retrieve the fog settings. The function
returns a 4 element 1D array with the following information:

-   \[0\] = enabled toggle (a
    [Boolean](../../../../../GameMaker_Language/GML_Overview/Data_Types)
    , either true or false ), default false
-   \[1\] =
    [Colour](../../../../../GameMaker_Language/GML_Reference/Drawing/Colour_And_Alpha/Colour_And_Alpha)
    , default c_black
-   \[2\] = start distance (
    [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)
    ), default 0
-   \[3\] = end distance (
    [Real](../../../../../GameMaker_Language/GML_Overview/Data_Types)
    ), default 1

Note that you can change these values and pass the full array to the [
gpu_set_fog() ](gpu_set_fog) function as a single argument.

#### Syntax:

``` gml
gpu_get_fog();
```

#### Returns:

``` gml
 Array

(4 elements only; see above for details)
```

#### Example:

``` gml
var fog_a = gpu_get_fog();
fog_a[1] = c_red;
gpu_set_fog(fog_a);
```

The above code gets the current fog settings and then sets the colour
element of the array to c_red before setting the fog again using the
changed array.
