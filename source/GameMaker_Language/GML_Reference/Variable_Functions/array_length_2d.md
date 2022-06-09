# array_length_2d  DEPRECATED 

**WARNING!** This function is deprecated (and replaced by
[array_length()](array_length) ) as arrays are no longer limited to
only 1 or 2 dimensions, and as such this function is only supplied for
support of legacy projects. All new projects should use the current way
of creating and accessing multi-dimension arrays (see
[here](../../GML_Overview/Arrays) for more information). With this
function you can get the length (number of entries) of a the second
dimension of an array. You supply the entry number for the first
dimension and the function will return the number of second dimension
entries that the array has (to find the length of the first dimension
use the function [ array_height_2D() ](array_height_2d) ). The
function will return 0 if the variable given is not an array or 1 if the
variable is a 1D array (as there is still 1 row).

#### Syntax:

``` gml
array_length_2d(array_index, n);
```

|             |                                                                      |                                              |
|-------------|----------------------------------------------------------------------|----------------------------------------------|
| Argument    | Type                                                                 | Description                                  |
| array_index |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)     | The index of the array to check.             |
| n           |  [Real](../../../../GameMaker_Language/GML_Overview/Data_Types)  | The entry of the array to get the length of. |

#### Returns:

``` gml
 Real
```

#### Example:

``` gml
for (var i = 0; i &amp;lt; array_height_2d(a); ++i;)
{
    for (var j = 0; j &amp;lt; array_length_2d(a, i); ++j;)
    {
        a[i, j] = -1;
    }
}
```

The above code will loop through a 2D array and set each entry to -1.
