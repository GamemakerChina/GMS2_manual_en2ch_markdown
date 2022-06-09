# array_height_2d  DEPRECATED 

**WARNING!** This function is deprecated (and replaced by
[array_length()](array_length) ) as arrays are no longer limited to
only 1 or 2 dimensions, and as such this function is only supplied for
support of legacy projects. All new projects should use the current way
of creating and accessing multi-dimension arrays (see
[here](../../GML_Overview/Arrays) for more information). With this
function you can get the height (number of entries) of a the first
dimension of a 2D array. You supply the array to check and the output
from the function tells you how many initial entries it contains. You
can get the number of entries for the second dimension of the array
using the function [ array_length_2d ](array_length_2d) .

#### Syntax:

``` gml
array_height_2d(array_index);
```

|             |                                                                   |                                  |
|-------------|-------------------------------------------------------------------|----------------------------------|
| Argument    | Type                                                              | Description                      |
| array_index |  [Array](../../../../GameMaker_Language/GML_Overview/Arrays)  | The index of the array to check. |

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
